
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