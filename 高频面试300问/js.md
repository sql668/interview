
1. 自定义数组的unshift方法
```js
Array.prototype.myUnshift = function(){
    const len = arguments.length;
    for(let i = len - 1; i >= 0; i--){
        this.splice(0, 0, arguments[i]);
    }
    return this.length;
}
```

2. 数组去重

```js

Array.prototype.myUnique = function(){
    return Array.form(new Set(this))
}

Array.prototype.myUnique = function(){
    let arr = [];
    for(let i = 0; i < this.length; i++){
        if(!arr.includes(this[i])){
            arr.push(this[i])
        }
    }
    return arr
}

Array.prototype.myUnique = function(){
    return this.filter((item, index) => this.indexOf(item) === index)
}

```

3. 打印100以内的质数

```js
function printPrimeNumbers() {
    for (let i = 2; i <= 100; i++) {
        let isPrime = true;
        for (let j = 2; j < i; j++) {
            if (i % j === 0) {
                isPrime = false;
                break;
            }
        }
        if (isPrime) {
            console.log(i);
        }
    }
}
```

4. 获取指定范围内的随机整数
   
```js
function getRandomInt(min, max) {
    min = Math.ceil(min); // 向上取整
    max = Math.floor(max);// 向下取整
    return Math.floor(Math.random() * (max - min + 1)) + min;
}

// 生成随机整数（包含性控制）
/**
 *  "[]"：包含两端（闭区间）
    "[)"：左闭右开区间
    "(]"：左开右闭区间
    "()"：不包含两端（开区间）
 */
function randomIntInRange(min, max, mode = "[]") {
  let offset = 0;
  if (mode.endsWith(")")) offset -= 1; // 右端不包含则减小范围
  if (mode.startsWith("(")) min += 1;  // 左端不包含则起始值+1

  return Math.floor(Math.random() * (max - min + offset + 1)) + min;
}
```

5. 获取URL中的参数

```js
let url = 'https://example.com?param1=value1&param2=value2_1&param2=value2_2';
function getUrlParams(url) {
  const paramsObj = {};
  try {
    const urlObj = new URL(url);
    const params = new URLSearchParams(urlObj.search);

    // 遍历所有唯一参数名
    const uniqueKeys = [...new Set(params.keys())];
    for (const key of uniqueKeys) {
      const values = params.getAll(key);
      paramsObj[key] = values.length > 1 ? values : values[0];
    }
  } catch (e) {
    console.error('Invalid URL:', e);
  }
  return paramsObj;
}
getUrlParams(url)
{
    "param1": "value1",
    "param2": [
        "value2_1",
        "value2_2"
    ]
}

/**
 * 使用正则表达式
 */
function getParamsRegExp(url) {
  const params = {};
  // [^…] 不在方括号里的任意字符
  const regex = /([^?&=]+)=([^&]+)/g;
  const matches = url.matchAll(regex);
  for (const match of matches) {
    const key = decodeURIComponent(match[1]);
    const value = decodeURIComponent(match[2]);
    params[key] = params[key] ? [].concat(params[key], value) : value;
  }
  return params;
}
```


6. 数组随机排序

```js   
// 方式一
function shuffleArray(arr) {
    return arr.sort(() => Math.random() - 0.5);
}
//方式二
function shuffleArray(arr) {
    for (let i = arr.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [arr[i], arr[j]] = [arr[j], arr[i]];
    }
    return arr;
}
```

7. 数组扁平化

```js
// 方式一
function flattenArray(arr) {
    return [].concat(...arr.map(item => Array.isArray(item) ? flattenArray(item) : item));
}

// 方式二   
function flattenArray(arr) {
    return arr.reduce((acc, val) => Array.isArray(val) ? acc.concat(flattenArray(val)) : acc.concat(val), []);
}

// 方式三
function flattenArray(arr) {
    while (arr.some(item => Array.isArray(item))) {
        arr = [].concat(...arr);
    }
    return arr;
}
```

8. 两数之和

给定一个整数数组 nums 和一个目标值 target，请你在该数组中找出和为目标值的那 两个 整数，并返回他们的数组下标。

```js
// 方式一
function twoSum(nums, target) {
    const numMap = new Map();
    for (let i = 0; i < nums.length; i++) {
        const complement = target - nums[i];
        if (numMap.has(complement)) {
            return [numMap.get(complement), i];
        }
        numMap.set(nums[i], i);
    }
    return [];
}

// 方式二
function twoSum (nums, target) {
  for (let i = 0; i < nums.length; i++) {
    const num = nums[i];
    const targetIndex = nums.indexOf(target - num, i + 1);
    if (targetIndex !== -1) {
      return [i, targetIndex];
    }
  }
  return [];
}
```

9. 给 a b c 三个请求，希望c在a,b获取后再请求

promise方式
```js
function requestA() {
  return new Promise((resolve) => {
    // 模拟请求a
    setTimeout(() => resolve('a完成'), 1000);
  });
}

function requestB() {
  return new Promise((resolve) => {
    // 模拟请求b
    setTimeout(() => resolve('b完成'), 1500);
  });
}

function requestC() {
  return new Promise((resolve) => {
    // 请求c的逻辑
    resolve('c完成');
  });
}

// 并行执行a和b，全部完成后执行c
Promise.all([requestA(), requestB()])
  .then(([resultA, resultB]) => {
    console.log(resultA, resultB); // 输出a和b的结果
    return requestC();
  })
  .then(resultC => console.log(resultC)); // 输出c的结果
```

10. 实现发布订阅
```js
class EventEmitter {
  constructor() {
    this.events = {};    // 存储事件及对应的回调列表，格式：{ eventName: [{ id, callback, once }] }
    this.callbackId = 0; // 回调唯一标识，用于精准取消订阅
  }

  /**
   * 订阅事件
   * @param {string} eventName 事件名称
   * @param {Function} callback 回调函数
   * @returns {number} 回调的唯一标识符，用于卸载订阅
   */
  on (eventName, callback,once = false) {
    if (!this.events[eventName]) this.events[eventName] = [];
    const id = ++this.callbackId;
    this.events[eventName].push({ id, callback, once });
    return id;
  }

  /**
   * 订阅一次事件（触发后自动取消）
   * @param {string} eventName 事件名称
   * @param {Function} callback 回调函数
   * @returns {number} 回调的唯一标识符
   */
  once (eventName, callback) {
    const id = this.on(eventName, (...args) => {
      callback(...args);
      this.off(eventName, id); // 执行后自动取消订阅
    },true);
    return id;
  }

  /**
   * 取消订阅
   * @param {string} eventName 事件名称
   * @param {number} id 回调的唯一标识符
   */
  off (eventName, id) {
    if (!this.events[eventName]) return;
    this.events[eventName] = this.events[eventName].filter(item => item.id !== id);
  }

  /**
   * 触发事件
   * @param {string} eventName 事件名称
   * @param {...any} args 传递给回调的参数
   */
  emit (eventName, ...args) {
    const listeners = this.events[eventName];
    if (!listeners) return;
    // 复制当前列表，避免执行过程中数组被修改
    [...listeners].forEach(({ callback }) => {
      callback(...args);
    });
  }
}
```

11. 导致页面加载白屏时间长的原因有哪些？怎么进行优化

白屏时间：指从用户发起请求到浏览器开始渲染页面内容所经历的时间(空白-》第一个画面出现的时间)。
重要性： 白屏时间是衡量网页性能的重要指标之一，直接影响用户体验。较长的白屏时间可能导致用户流失，因为用户通常期望网页能够快速响应和加载。
导致白屏时间长的原因有很多，常见的包括：1. 网络问题：如网络带宽太小、网络延迟过高、服务器响应时间过长等；2. 服务器问题：如服务器负载过高、数据库查询超时等；3. 静态资源加载问题：如静态资源CDN配置错误、静态资源加载超时等；4. 页面渲染问题：如页面布局、样式、脚本等加载时间过长等。


优化策略：
1. 使用CDN加速静态资源加载；
2. 合理使用缓存机制，减少重复请求；
3. 对关键资源进行预加载或预解析；
4. 优化CSS和JavaScript的加载顺序，避免阻塞渲染；
5. 使用骨架屏或占位图提升用户体验。

