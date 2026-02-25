MENG-ADMIN-REACT

package.json
```json
{
  "name": "meng-react-admin",
  "private": true,
  "version": "0.0.0",
  "type": "module",
  "homepage": ".",
  "scripts": {
    "prepare": "husky",
    "cz": "czg",
    "dev": "vite",
    "build": "tsc && vite build",
    "lint": "eslint . --ext ts,tsx --report-unused-disable-directives --max-warnings 0",
    "lint:fix": "eslint . --ext .js,.jsx,.ts,.tsx ./ --fix",
    "changelog": "conventional-changelog -p angular -i Changelog.md -s -r 0",
    "preview": "vite preview",
    "push": "git add . && czg && git push",
    "gen:icon": "esno ./build/generate/icon/index.ts"
  },
  "dependencies": {
    "@ant-design/compatible": "^5.1.3",
    "@ant-design/cssinjs": "^1.18.4",
    "@ant-design/icons": "^5.3.1",
    "@ant-design/x": "^1.6.0",
    "@ctrl/tinycolor": "^4.0.3",
    "@emotion/react": "^11.11.3",
    "@emotion/styled": "^11.11.0",
    "@fdesign/component": "0.0.2",
    "@fdesign/util": "^0.0.1",
    "@form-created/core": "0.0.1-beta.6",
    "@form-created/formily-antd": "0.0.1-beta.6",
    "@form-created/formily-setters": "0.0.1-beta.6",
    "@form-created/formily-transformer": "0.0.1-beta.6",
    "@form-created/react": "0.0.1-beta.6",
    "@form-created/react-settings-form": "0.0.1-beta.6",
    "@form-created/shared": "0.0.1-beta.6",
    "@formily/antd-v5": "^1.2.0",
    "@formily/core": "^2.3.1",
    "@formily/json-schema": "^2.3.1",
    "@formily/path": "^2.3.1",
    "@formily/react": "^2.3.1",
    "@formily/reactive": "^2.3.1",
    "@formily/reactive-react": "^2.3.1",
    "@formily/shared": "^2.3.1",
    "@iconify/iconify": "^3.1.1",
    "@juggle/resize-observer": "^3.4.0",
    "@monaco-editor/loader": "^1.3.3",
    "@monaco-editor/react": "^4.5.1",
    "@rc-utils/hooks": "1.0.1-rc.1",
    "@tanstack/react-query": "^5.24.1",
    "@tanstack/react-query-devtools": "^5.34.1",
    "ahooks": "^3.7.10",
    "antd": "^5.26.7",
    "antd-style": "^3.6.1",
    "axios": "^1.6.7",
    "classnames": "^2.5.1",
    "dateformat": "^5.0.3",
    "dayjs": "^1.11.10",
    "dexie": "^3.2.5",
    "dexie-react-hooks": "^1.1.7",
    "immer": "^10.0.3",
    "js-cookie": "^3.0.5",
    "lib": "link:@ant-design/compatible/lib",
    "lodash-es": "^4.17.21",
    "nanoid": "^5.0.6",
    "nprogress": "^0.2.0",
    "path-to-regexp": "^6.2.1",
    "qs": "^6.11.2",
    "rc-util": "^5.39.1",
    "react": "^18.3.1",
    "react-activation": "^0.12.4",
    "react-color": "^2.19.2",
    "react-dom": "^18.3.1",
    "react-error-boundary": "^4.0.13",
    "react-fast-compare": "^3.2.2",
    "react-router": "^6.22.1",
    "react-router-dom": "^6.22.1",
    "react-transition-group": "^4.4.5",
    "react-use": "^17.5.0",
    "resize-observer-polyfill": "^1.5.1",
    "screenfull": "^6.0.2",
    "unocss": "^0.58.5",
    "zustand": "^4.5.0"
  },
  "devDependencies": {
    "@babel/parser": "^7.22.10",
    "@commitlint/cli": "18.6.1",
    "@commitlint/config-conventional": "18.6.2",
    "@iconify/json": "^2.2.187",
    "@originjs/vite-plugin-commonjs": "^1.0.3",
    "@purge-icons/generated": "^0.10.0",
    "@tanstack/eslint-plugin-query": "^5.32.1",
    "@types/fs-extra": "^11.0.4",
    "@types/inquirer": "^9.0.7",
    "@types/js-cookie": "^3.0.6",
    "@types/lodash-es": "^4.17.12",
    "@types/node": "^20.11.25",
    "@types/nprogress": "^0.2.3",
    "@types/qs": "^6.9.12",
    "@types/react": "^18.2.43",
    "@types/react-color": "^2.17.11",
    "@types/react-dom": "^18.2.17",
    "@types/react-transition-group": "^4.4.10",
    "@typescript-eslint/eslint-plugin": "^6.14.0",
    "@typescript-eslint/parser": "^6.14.0",
    "@unocss/preset-icons": "^0.58.5",
    "@unocss/preset-rem-to-px": "^0.58.5",
    "@unocss/reset": "^0.58.5",
    "@unocss/transformer-attributify-jsx": "^0.58.5",
    "@vitejs/plugin-legacy": "^5.3.1",
    "@vitejs/plugin-react": "^4.2.1",
    "@vitejs/plugin-react-swc": "^3.7.1",
    "@welldone-software/why-did-you-render": "^8.0.1",
    "autoprefixer": "^10.4.17",
    "chalk": "^5.3.0",
    "cz-git": "1.8.0",
    "czg": "1.8.0",
    "eslint": "^8.55.0",
    "eslint-config-prettier": "^9.1.0",
    "eslint-plugin-prettier": "^5.1.3",
    "eslint-plugin-react-hooks": "^4.6.0",
    "eslint-plugin-react-refresh": "^0.4.5",
    "esno": "^4.7.0",
    "fs-extra": "^11.2.0",
    "husky": "^9.0.11",
    "inquirer": "^9.2.20",
    "lint-staged": "^15.2.2",
    "prettier": "^3.2.5",
    "rollup-plugin-gzip": "^3.1.1",
    "sass": "^1.71.1",
    "tailwindcss": "^3.4.1",
    "typescript": "^5.2.2",
    "vite": "^5.2.10",
    "vite-plugin-purge-icons": "^0.10.0",
    "vite-plugin-require-transform": "^1.0.21",
    "vite-plugin-svg-icons": "^2.0.1"
  },
  "config": {
    "commitizen": {
      "path": "node_modules/cz-git"
    }
  },
  "lint-staged": {
    "src/**/*.{js,jsx,ts,tsx,json,md}": [
      "eslint --fix"
    ]
  }
}

```


# 1. svg图标生成

- 1. 进入icon目录，执行命令：

```bash
npm install vite-plugin-svg-icons -D
# 或
yarn add vite-plugin-svg-icons -D
```

- 2. 修改vite.config.ts文件

```typescript
import fs from 'fs'
import path, { resolve } from 'path'
import { defineConfig, loadEnv } from 'vite'
import react from '@vitejs/plugin-react'
import UnoCSS from 'unocss/vite'
import gzipPlugin from 'rollup-plugin-gzip'
import legacy from '@vitejs/plugin-legacy'
import { createSvgIconsPlugin } from 'vite-plugin-svg-icons' // 封装svg图标
import requireTransform from 'vite-plugin-require-transform'
import PurgeIcons from 'vite-plugin-purge-icons'
import { theme } from 'antd/lib'
import { convertLegacyToken } from '@ant-design/compatible/lib'
const { defaultAlgorithm, defaultSeed } = theme

const mapV5Token = defaultAlgorithm(defaultSeed)
const v5Vars = convertLegacyToken(mapV5Token)
const json = JSON.stringify(v5Vars, null, 2)
// 写入文件
fs.writeFile('antdV5Vars.json', json, (err) => {
  if (err) {
    console.error(err)
    return
  }
})

export default defineConfig((config) => {
  const root = process.cwd()
  const env = loadEnv(config.mode, root)

  return {
    base: env.VITE_BASE_URL,
    optimizeDeps: {
      include: ['@iconify/iconify'],
    },
    build: {
      minify: 'terser',
      terserOptions: {
        compress: {
          drop_console: config.mode === 'production', //生产环境删除console和debugger
          drop_debugger: config.mode === 'production',
        },
      },
      rollupOptions: {
        output: {
          manualChunks: {
            react: ['react', 'react-dom', 'react-router', 'react-router-dom'], // 将react和react-dom打包到vendor chunk中
            antd: ['antd', '@ant-design/icons'], // 将antd打包到antd chunk中
            formily: ['@formily/antd-v5', '@formily/core', '@formily/react', '@formily/reactive'],
          },
        },
      },
    },
    css: {
      preprocessorOptions: {
        scss: {//scss全局变量
          additionalData: '@import "@/style/var.scss";',//在每个scss文件中自动引入var.scss
          javascriptEnabled: true,//允许在scss文件中使用javascript表达式，如@import (reference) "xxx";，需要开启此选项
        },
      },
    },
    resolve: {
      alias: {
        '@': resolve(__dirname, './src'),
      },
    },
    plugins: [
      react(),
      UnoCSS(),
      gzipPlugin(),
      legacy({
        targets: ['> 2%', 'last 2 versions and not dead'],
      }),
      createSvgIconsPlugin({//svg图标插件
        iconDirs: [path.resolve(process.cwd(), 'src/assets/icons')],
        symbolId: 'icon-[dir]-[name]',
      }),
      PurgeIcons(),
      //requireTransform({ fileRegex: /.ts$|.tsx$|.js$|.jsx/ }),
      requireTransform({ fileRegex: /^(?!.*node_modules).*\.(js|jsx|ts|tsx)$/ }),
      //viteCommonjs(), //支持require语法
    ],
    define: {
      __PACKAGE_NAME__: JSON.stringify(process.env.npm_package_name),
    },
    server: {
      port: 5174,
      proxy: {
        '/api': {
          target: 'http://127.0.0.1:8090', // 目标服务器的地址
          //changeOrigin: true, // 是否改变源地址
          //rewrite: (path) => path.replace(/^\/api/, ''), // 重写路径
        },
      },
    },
  }
})

```

- 3. 图标注册
在项目入口文件（如main.ts）中引入注册模块
```typescript
import 'virtual:svg-icons-register';
```

- 4. SVG图标组件实现

```tsx
import { useMemo } from 'react'
import { createStyles } from 'antd-style'
export interface propsInterface {
  /** src/assets/icons目录下的svg文件名称 */
  icon: string
  /** 图标大小 */
  size?: string | number
  color?: string
  profix?: string
  className?: string
  [key: string]: any
}

const useStyles = createStyles(({ css }, props: { size: number | string; color: string }) => {
  const { size, color } = props
  let s = `${size}`
  s = `${s.replace('px', '')}px`
  return {
    container: css`
      width: ${s};
      height: ${s};
      color: ${color};
    `,
  }
})

export function SvgIcon(props: propsInterface) {
  const { size = 16, color = '', profix = 'icon', icon, className, ...restProps } = props
  const { styles, cx } = useStyles({ size, color })
  const iconName = useMemo<string>(() => {
    return `#${profix}-${icon}`
  }, [profix, icon])

  return (
    <svg aria-hidden='true' className={cx(styles.container, className)} {...restProps}>
      <use href={iconName} />
    </svg>
  )
}

```

# 2. iconify图标生成以及图标选择器

- 1. 安装依赖

```bash
npm install @iconify/json @iconify/iconify
```

- 2. 图标集预生成
该命令会生成所选择的图标集
```json
"scripts": {
    "gen:icon": "esno ./build/generate/icon/index.ts"
}
```
build/generate/icon/index.ts
```ts
import path from 'path'
import fs from 'fs-extra'
import inquirer from 'inquirer'
import chalk from 'chalk'
import pkg from '../../../package.json'

async function generateIcon() {
  const dir = path.resolve(process.cwd(), 'node_modules/@iconify/json')

  const raw = await fs.readJSON(path.join(dir, 'collections.json'))

  const collections = Object.entries(raw).map(([id, v]) => ({
    ...(v as any),
    id,
  }))

  const choices = collections.map((item) => ({ key: item.id, value: item.id, name: item.name }))

  inquirer
    .prompt([
      {
        type: 'list',
        name: 'useType',
        choices: [
          { key: 'local', value: 'local', name: 'Local' }, //本地模式
          { key: 'onLine', value: 'onLine', name: 'OnLine' },//在线模式，包含图标集前缀和图标名称，会远程请求图标数据
        ],
        message: 'How to use icons?',
      },
      {
        type: 'list',
        name: 'iconSet',
        choices: choices,// 选择图标集，如：ant-design、mdi、fa-solid等
        message: 'Select the icon set that needs to be generated?',
      },
      {
        type: 'input',
        name: 'output',
        message: 'Select the icon set that needs to be generated?',// 输出目录，默认为src/components/Icon/data
        default: 'src/components/Icon/data',
      },
    ])
    .then(async (answers) => {
      const { iconSet, output, useType } = answers
      const outputDir = path.resolve(process.cwd(), output)
      fs.ensureDir(outputDir)
      const genCollections = collections.filter((item) => [iconSet].includes(item.id))
      const prefixSet: string[] = []
      for (const info of genCollections) {
        const data = await fs.readJSON(path.join(dir, 'json', `${info.id}.json`))
        if (data) {
          const { prefix } = data
          const isLocal = useType === 'local'
          const icons = Object.keys(data.icons).map(
            (item) => `${isLocal ? prefix + ':' : ''}${item}`,
          )

          await fs.writeFileSync(
            path.join(output, `icons.data.ts`),
            `export default ${isLocal ? JSON.stringify(icons) : JSON.stringify({ prefix, icons })}`,
          )
          prefixSet.push(prefix)
        }
      }
      fs.emptyDir(path.join(process.cwd(), 'node_modules/.vite'))
      console.log(
        `✨ ${chalk.cyan(`[${pkg.name}]`)}` + ' - Icon generated successfully:' + `[${prefixSet}]`,
      )
    })
}

generateIcon()

```
- 3. 图标化
项目中使用到的是vite-plugin-purge-icons这个插件来进行图标实现。

```bash
yarn add @iconify/iconify

yarn add @iconify/json @purge-icons/generated -D
```
vite.config.ts中已经引入了vite-plugin-purge-icons插件，接下来就是图标组件的实现了。
```ts
import PurgeIcons from 'vite-plugin-purge-icons';

export default {
  plugins: [PurgeIcons()],
};

```
组件实现
```tsx
import { useEffect, useRef } from 'react'
//import Iconify from '@purge-icons/generated'
import Iconify from '@iconify/iconify'
import { isString } from 'lodash-es'
import { SvgIcon } from '../svg'
import { createStyles } from 'antd-style'
export interface IconType {
  icon: string
  color?: string
  size?: number | string
  mode?: 'iconify' | 'svg'
  className?: string
  [key: string]: any
}
const SVG_END_WITH_FLAG = '|svg'
const useStyles = createStyles(({ css }, props: { size: number | string; color: string }) => {
  const { size, color } = props
  let fs = size
  if (isString(size)) {
    fs = parseInt(size, 10)
  }
  return {
    container: css`
      font-size: ${fs}px;
      color: ${color};
      display: inline-flex;
      align-items: center;
      line-height: 0;
      text-align: center;
    `,
  }
})

export function Icon(props: IconType) {
  const { icon, color = '', size = 16, mode = 'iconify', className, ...restProps } = props
  const iconRef = useRef(null)
  const { styles, cx } = useStyles({ size, color })

  useEffect(() => {
    if (mode != 'svg' && !icon?.endsWith(SVG_END_WITH_FLAG)) {
      const el = iconRef.current! as HTMLElement
      const svg = Iconify.renderSVG(icon, {})
      if (svg) {
        el.textContent = ''
        el.appendChild(svg)
      } else {
        const span = document.createElement('span')
        span.className = 'iconify'
        span.dataset.icon = icon
        el.textContent = ''
        el.appendChild(span)
      }
    }
  }, [icon, mode])
  return mode === 'svg' || icon?.endsWith(SVG_END_WITH_FLAG) ? (
    <SvgIcon
      icon={icon?.endsWith(SVG_END_WITH_FLAG) ? icon.replace(SVG_END_WITH_FLAG, '') : icon}
      color={color}
      size={size}
      {...restProps}></SvgIcon>
  ) : (
    <span ref={iconRef} className={cx(styles.container, className, 'anticon')}></span>
  )
}

```
-4. 图标选择器
图标选择器的实现比较简单，直接使用antd的Select组件进行图标选择
```tsx
//import iconData from '../data'
import { Select } from 'antd'
import defaultIcon from '../data'
import { createStyles } from 'antd-style'
import svgIcons from 'virtual:svg-icons-names'
import { Icon } from '../icon'
import { useEffect, useState } from 'react'
import type { SelectProps } from 'antd/es/select'

function getIconifyIcons() {
  return defaultIcon.map((item) => {
    const prefix = item.prefix
    return {
      label: <span>{item.prefix}</span>,
      title: item.prefix,
      options: item.icons.map((icon) => {
        return {
          label: (
            <div className='iconify-select-item'>
              <Icon
                icon={`${prefix}:${icon}`}
                size={16}
                className='iconify-select-item-icon'></Icon>
              <span className='iconify-select-item-label'>{`${prefix}:${icon}`}</span>
            </div>
          ),
          value: `${prefix}:${icon}`,
        }
      }),
    }
  })
}

function getSvgIcons() {
  //return svgIcons.map((icon: string) => icon.replace('icon-', ''));
  return svgIcons.map((icon: string) => {
    return {
      label: (
        <div className='iconify-select-item'>
          <Icon
            icon={`${icon.replace('icon-', '')}|svg`}
            size={16}
            className='iconify-select-item-icon'></Icon>
          <span className='iconify-select-item-label'>{icon.replace('icon-', '')}</span>
        </div>
      ),
      value: `${icon.replace('icon-', '')}|svg`,
    }
  })
}

const iconData = getIconifyIcons()
const svgData = getSvgIcons()

const useStyles = createStyles(({ css }) => {
  return {
    container: css`
      min-width: 120px;
    `,
  }
})

export interface IconSelectProps extends SelectProps {
  iconMode?: 'iconify' | 'svg'
  [key: string]: any
}

export function IconSelect(props: IconSelectProps) {
  const { styles, cx } = useStyles()
  const [options, SetOptions] = useState(iconData)
  const { iconMode = 'iconify', ...restProps } = props
  useEffect(() => {
    if (iconMode === 'svg') {
      SetOptions(svgData as any)
    } else {
      SetOptions(iconData)
    }
  }, [iconMode])
  return <Select options={options as any} className={cx(styles.container)} {...restProps}></Select>
}

```

# 3. 路由缓存KeepAlive
路由缓存的实现主要是通过react-activation这个库来实现的，react-activation是一个基于react的组件缓存库，可以实现组件的缓存和恢复，类似于vue中的keep-alive组件。react-activation的使用比较简单，只需要在需要缓存的组件上添加`<KeepAlive>`组件即可。

用 <KeepAlive> 包裹需要保持状态的组件
```tsx
import { KeepAlive } from 'react-activation'
export const LoadView = (props: RouterVo) => {
  if (props.handle.component === 'Layout') {
    return null
  } else if (props.handle.component === 'IFrame') {
    return <IframeLayout></IframeLayout>
  }

  if (props.handle.isKeepAlive) {
    return (
      <KeepAlive cacheKey={props.path} name={props.path}>
        {LazyLoad(lazy(modules[`/src${props.handle.component}.tsx`] as any))}
      </KeepAlive>
    )
  }

  return LazyLoad(lazy(modules[`/src${props.handle.component}.tsx`] as any))
}
```
在不会被销毁的位置放置 <AliveScope> 外层，一般为应用入口处
```tsx
import { AliveScope } from 'react-activation'
ReactDOM.createRoot(document.getElementById('root')!).render(
  <QueryClientProvider client={queryClient}>
    <ReactQueryDevtools initialIsOpen={false} />
    <AliveScope>
      <App />
    </AliveScope>
  </QueryClientProvider>,
)
```

useTabs tab级别页面缓存
```tsx
import { useCallback, useEffect, useState } from 'react'
import useMatchRoute from './useMatchRoute'
import { useNavigate } from 'react-router-dom'
import { useAliveController } from 'react-activation'
import {
  setTags as setTabs,
  removeTag,
  useTagsTabStore,
  removeOtherTag,
  updateTag,
} from '@/store/tagsView'

function getKey() {
  return new Date().getTime().toString()
}

export function useTabs() {
  // 当前打开的tab页签
  const tabs = useTagsTabStore.use.tags()
  const homePath = useTagsTabStore.use.defaultTag()

  // 当前激活的tab
  const [activeTabRoutePath, setActiveTabRoutePath] = useState<string>('')

  // 当前匹配的路由
  const matchRoute = useMatchRoute()

  const navigate = useNavigate()

  const { getCachingNodes, drop, refresh } = useAliveController()

  // 关闭tab页签
  const closeTab = useCallback(
    (routePath?: string) => {
      if (!routePath) {
        routePath = activeTabRoutePath
      }
      const cachingNodes = getCachingNodes()
      // 不能关闭首页
      if (routePath === homePath) return
      const index = tabs.findIndex((o) => o.routePath === routePath)
      if (tabs[index].routePath === activeTabRoutePath && tabs.length > 1) {
        if (index > 0) {
          navigate(tabs[index - 1].routePath)
        } else {
          navigate(tabs[index + 1].routePath)
        }
      }
      const cache = cachingNodes.find((item) => item.cacheKey === routePath)
      if (cache) {
        // 关闭的页面开启了缓存，需要将该页面从缓存中删除
        drop(cache.name!)
      }
      removeTag(index)
    },
    [activeTabRoutePath],
  )
  // 刷新页面
  const refreshTab = useCallback(
    (routePath?: string) => {
      if (!routePath) {
        routePath = activeTabRoutePath
      }
      const cachingNodes = getCachingNodes()
      const cache = cachingNodes.find((item) => item.cacheKey === routePath)
      refresh(cache?.name!)
      if (cache) {
        // 关闭的页面开启了缓存，需要将该页面从缓存中删除
        refresh(cache.name!)
      } else {
        const index = tabs.findIndex((tab) => tab.routePath === routePath)
        if (index >= 0) {
          // 这个是react的特性，key变了，组件会卸载重新渲染
          updateTag(index, {
            ...tabs[index],
            key: getKey(),
          })
        }
      }
      // 增加重定向操作，使页面刷新出现切换的效果，也可以注释掉该操作
      navigate(`/redirect${routePath}${location.search}`)
    },
    [activeTabRoutePath],
  )
  // 关闭其他页面
  const closeOtherTab = (routePath?: string) => {
    if (!routePath) {
      routePath = activeTabRoutePath
    }
    const cachingNodes = getCachingNodes()
    tabs.forEach((tab) => {
      if (tab.routePath !== routePath && routePath !== homePath) {
        const cache = cachingNodes.find((item) => item.name === tab.routePath)
        if (cache) {
          // 关闭的页面开启了缓存，需要将该页面从缓存中删除
          drop(cache.name!)
        }
      }
    })
    removeOtherTag(routePath)
  }

  const activeTab = tabs.find((item) => item.routePath === activeTabRoutePath)

  useEffect(() => {
    if (!matchRoute) return
    if (matchRoute.handle?.title == '404' || matchRoute.handle?.title == 'redirect') return

    if (matchRoute.handle?.redirect) return
    const existKeepAliveTab = tabs.find((item) => item.routePath === matchRoute.routePath)
    if (!existKeepAliveTab) {
      setTabs([
        ...tabs,
        {
          title: matchRoute.title,
          key: getKey(),
          routePath: matchRoute.routePath,
          pathname: matchRoute.pathname,
          //children: matchRoute.children,  zuztand 不能添加children,否则会报错
          handle: matchRoute.handle,
        },
      ])
    }
    // TODO tabs中存在当前路由，但是路由参数不同，可以刷新该路由
    setActiveTabRoutePath(matchRoute.routePath)
    // eslint-disable-next-line react-hooks/exhaustive-deps
  }, [matchRoute])

  return {
    tabs,
    setTabs,
    activeTabRoutePath,
    closeTab,
    refreshTab,
    closeOtherTab,
    activeTab,
  }
}

```

# 4. 动态菜单/动态路由 实现

路由组件 Router.ts
```tsx
import { antdUtils } from '@/utils/antdUtil'
import { App } from 'antd'
import { lazy, useEffect } from 'react'
import { RouterProvider } from 'react-router-dom'
import { router } from './baseRouter'
import KeepAlive from 'react-activation'
import LazyLoad from '@/components/lazy'

import { RouterVo } from '@/types/model/routerVo'
import { IframeLayout } from '@/layout/iframe'

const Router = () => {
  const { notification, message, modal } = App.useApp()

  useEffect(() => {
    antdUtils.setMessageInstance(message)
    antdUtils.setNotificationInstance(notification)
    antdUtils.setModalInstance(modal)
  }, [notification, message, modal])

  return <RouterProvider router={router} />
}

// 批量导入
const modules = import.meta.glob('@/views/**/*/index.tsx')

export const LoadView = (props: RouterVo) => {

  if (props.handle.component === 'Layout') {
    return null
  } else if (props.handle.component === 'IFrame') {
    return <IframeLayout></IframeLayout>
  }

  if (props.handle.isKeepAlive) {
    return (
      <KeepAlive cacheKey={props.path} name={props.path}>
        {LazyLoad(lazy(modules[`/src${props.handle.component}.tsx`] as any))}
      </KeepAlive>
    )
  }

  return LazyLoad(lazy(modules[`/src${props.handle.component}.tsx`] as any))
}

export default Router

```

组装路由数据
```tsx
import MengLayout from '@/layout'
import NotAuth from '@/views/403'
import NotFound from '@/views/errors/404'
import NotNotWork from '@/views/500'
import Login from '@/views/login'
import Register from '@/views/register'
import { Navigate, RouteObject, createBrowserRouter } from 'react-router-dom'
import RouterErrorElement from '@/views/router-error-element'
import { RouterVo } from '@/types/model'
import CreatedForm from '@/views/tool/form/views/edit'

// 静态路由数据，包含登录、注册、404、403、500等页面，这些页面不需要权限控制，直接放在路由数据中
export const StaticRoute: RouteObject[] = [
  {
    index: false,
    path: '/login',
    element: <Login></Login>,
    handle: {
      title: '登录',
      fullPath: '/login',
    },
  },
  {
    path: '/form-created',
    element: <CreatedForm></CreatedForm>,
    handle: {
      title: '表单测试',
      fullPath: '/form-created',
    },
  },
  {
    path: '/register',
    element: <Register></Register>,
    handle: {
      title: '注册',
      fullPath: '/register',
    },
  },
  {
    path: '/403',
    element: <NotAuth></NotAuth>,
    handle: {
      title: '403',
      fullPath: '/403',
    },
  },
  {
    path: '/404',
    element: <NotFound></NotFound>,
    handle: {
      title: '404',
      fullPath: '/404',
    },
  },
  {
    path: '/500',
    element: <NotNotWork></NotNotWork>,
    handle: {
      title: '500',
      fullPath: '/500',
    },
  },
]

export const routerData: RouteObject[] = [
  {
    path: '/',
    element: <Navigate to='/redirect' replace />,
  },
  ...StaticRoute,
  {// 将其他页面匹配到layout中，由layout进行权限控制和路由分发
    path: '*',
    //element: <NotFound></NotFound>,
    element: <MengLayout></MengLayout>, // 初始时先其他页面渲染到MengLayout中，由MengLayout进行路由分发，后续可以根据接口返回的路由数据进行动态路由的添加和替换
    errorElement: <RouterErrorElement></RouterErrorElement>,
  },
]

export const router = createBrowserRouter(routerData, {
  basename: import.meta.env.VITE_BASE_URL,
}) as any

function findNodeByPath(routes: RouteObject[], path: string) {
  for (let i = 0; i < routes.length; i += 1) {
    const element = routes[i]

    if (element.path === path) return element

    findNodeByPath(element.children || [], path)
  }
}

export const addRoutes = (parentPath: string, routes: RouteObject[]) => {
  if (!parentPath) {
    router.routes.push(...(routes as any))
    return
  }

  const curNode = findNodeByPath(router.routes, parentPath)

  if (curNode?.children) {
    curNode?.children.push(...routes)
  } else if (curNode) {
    curNode.children = routes
  }
}

export const replaceRoutes = (parentPath: string, routes: RouteObject[]) => {
  if (!parentPath) {
    router.routes.push(...(routes as any))
    return
  }

  const curNode = findNodeByPath(router.routes, parentPath)

  if (curNode) {
    router.routes.splice(router.routes.indexOf(curNode as any), 1, ...(routes as any))
    //curNode.children = routes
  }
}

export const restRoutes = (routes: RouteObject[]) => {
  router.routes.splice(0, router.routes.length, ...(routes as any))
}

export const staticRouteData: RouterVo[] = StaticRoute.map((item) => {
  return {
    path: item.path!,
    handle: item.handle,
  }
})

```

MengLayout.tsx
```tsx
import AuthRouter from '@/components/authRouter'
import BaseLayout from '@/layout/default'
import { usePermissionStore } from '@/store/permission'
import { MenuDataItem } from '@/types/menu'
import { memo, useCallback, useEffect, useMemo, useState } from 'react'
import { getMatchMenu, getMenuData as getMenuDataTrans, ishttp } from '@/utils/menu'
import { useLocation, useNavigate } from 'react-router-dom'
import { useDeepMemo } from '@/hooks/useMemo'
import { MenuContext } from '@/context/menu'
import useRouter from '@/hooks/useRouter'


function MengLayout() {
  const { pathname } = useLocation()

  useRouter()

  useEffect(() => {
    setLocation({ pathname: pathname })
  }, [pathname])
  const nav = useNavigate()
  const allRouters = usePermissionStore.use.routes()

  const [location, setLocation] = useState<{ pathname: string }>({ pathname: '/' })

  // 菜单相关数据
  const menuContextValue = useDeepMemo(() => {
    return {
      menuItemClick,
      menuData: menuData,
      matchMenuKeys: matchMenuKeys,
    }
  }, [menuItemClick, menuData, matchMenuKeys])
  const { matchRoutes } = useRouter()
  return (
    <AuthRouter>
      <MenuContext.Provider value={menuContextValue}>
        {matchRoutes.at(-1)?.handle.hasLayout && <BaseLayout></BaseLayout>}
      </MenuContext.Provider>
    </AuthRouter>
  )
}

export default memo(MengLayout)

```

useRouter.ts 获取路由数据，包含静态路由和接口返回到动态路由
```ts
import { staticRouteData } from '@/router/baseRouter'
import { useRouterStore } from '@/store/router'
import { getMatchRoute } from '@/utils/route'
import { useMemo } from 'react'
import { useLocation } from 'react-router'

function useRouter() {
  const { pathname } = useLocation()
  // 动态路由数据,接口返回到菜单数据
  const apiRouters = useRouterStore.use.allRouters()
  const allRouters = useMemo(
    () =>
      staticRouteData.concat(apiRouters, [
        {
          path: '/redirect',
          handle: {
            title: 'redirect',
            hasLayout: true,
          },
        },
        {
          path: '/redirect/*',
          handle: {
            title: 'redirect',
            hasLayout: true,
          },
        },
      ]),
    [apiRouters],
  )
  const matchRoutes = useMemo(
    () => getMatchRoute(pathname, allRouters, true),
    [pathname, allRouters],
  )
  return {
    matchRoutes,
  }
}

export default useRouter

```

AuthRouter.tsx 权限路由组件
```tsx
import { RouteObject, useLocation, useNavigate } from 'react-router-dom'
import { LOGIN_PATHNAME, TOKEN } from '@/config/config'
import { useEffect } from 'react'
import { Session } from '@/utils/storage'
import { permissions, useUserStore } from '@/store/user'
import { getInfoApi } from '@/api/common'
import { replaceRoutes, router } from '@/router/baseRouter'
import NotFound from '@/views/errors/404'
import { getRoutersApi } from '@/api/system/menu'
import { LoadView } from '@/router'
import MengLayout from '@/layout'
import { setPermissionRouters } from '@/store/permission'
import { RedirectView } from '@/views/redirect'
import { setDefaultTag } from '@/store/tagsView'
import { RouterVo } from '@/types/model/routerVo'
import { setRouters } from '@/store/router'
const whiteList = ['/login', '/register']

// 处理路由数据，将菜单数据处理成路由数据
const handleElement = (data: RouterVo[]) => {
  const result: RouteObject[] = []
  for (let i = 0; i < data.length; i++) {
    if (data[i].handle.hasLayout && !data[i].path.includes('/noLayout')) {
      const r: RouteObject = {
        path: `${data[i].path}`,
        element: LoadView(data[i]),
        id: `${data[i].path}`,
        handle: data[i].handle,
      }
      if (data[i].children && data[i].children!.length > 0) {
        r.children = handleElement(data[i].children!)
      }
      result.push(r)
    }
  }
  return result
}

const handleNoLayoutElement = (data: RouterVo[]) => {
  const result: RouteObject[] = []
  for (let i = 0; i < data.length; i++) {
    if (!data[i].handle.hasLayout) {
      const r: RouteObject = {
        path: `${data[i].path}`,
        element: LoadView(data[i]),
        id: `${data[i].path}`,
        handle: data[i].handle,
      }
      if (data[i].children && data[i].children!.length > 0) {
        r.children = handleNoLayoutElement(data[i].children!)
      }
      result.push(r)
    }
    if (data[i].children && data[i].children!.length > 0) {
      result.push(...handleNoLayoutElement(data[i].children!))
    }
  }
  return result
}

/**
 * 路由守卫
 * @param props
 * @returns
 */
export default function AuthRouter(props: { children: JSX.Element }) {
  const nav = useNavigate()
  const { pathname } = useLocation()
  useEffect(() => {
    if (!Session.get(TOKEN)) {
      if (whiteList.indexOf(pathname) === -1) {
        // 没有用户信息并且不在白名单中，重定向到登录页面
        nav(`${LOGIN_PATHNAME}?redirect=${encodeURIComponent(pathname)}`)
      }
    } else {
      if (
        (pathname !== LOGIN_PATHNAME || whiteList.indexOf(pathname) === -1) &&
        permissions().length === 0
      ) {
        // 没有用户信息，重新获取用户信息和权限
        getInfoApi().then((res) => {
          if (res.code === 0) {
            useUserStore.setState({
              user: res.data?.user,
              roles: res.data?.roles,
              permissions: res.data?.permissions,
            })
            if (res.data?.user.role.defaultRouter) {
              // 设置首页地址
              setDefaultTag(res.data?.user.role.defaultRouter)
            }
            // 获取路由数据
            getRoutersApi().then((res) => {
              if (res.code === 0) {
                setPermissionRouters(res.data || [])
                setRouters(res.data || [])

                const routers = handleElement(res.data || [])
                const nolayout = handleNoLayoutElement(res.data || [])
                //将路由数据添加到路由中
                replaceRoutes('*', [
                  ...nolayout,
                  {
                    id: '/',
                    path: '/',
                    element: <MengLayout></MengLayout>,
                    children: [
                      {
                        id: '/redirect',
                        path: '/redirect/*',
                        element: <RedirectView></RedirectView>,
                        handle: {
                          title: 'redirect',
                          fullPath: '/redirect',
                        },
                      },
                      ...routers,
                    ],
                  },

                  {
                    id: '*',
                    path: '*',
                    element: <NotFound></NotFound>,
                    handle: {
                      path: '404',
                      name: '404',
                      title: '404',
                    },
                  },
                ])
                const path = `${location.pathname}${location.search}`

                console.log(router.routes)
                // replace一下当前路由，为了触发路由匹配
                router.navigate(path.replace(import.meta.env.VITE_BASE_URL, '/'), { replace: true })
              }
            })
          }
        })
      }
    }
    // eslint-disable-next-line react-hooks/exhaustive-deps
  }, [pathname])
  return props.children
}

```

BaseLayout.tsx

```tsx
import { useDesign } from '@/hooks/useDesign'
import { Layout } from 'antd'
import { memo } from 'react'
import { MultipleHeader, LayoutHeader } from './header'
import LayoutContent from '../components/content'
import LayoutFooter from '../components/footer'
import { useDeepMemo } from '@/hooks/useMemo'
import classNames from 'classnames'
import LayoutSider from './sider'
import './_style.scss'
import { useHeaderSetting } from '@/hooks/setting/useHeaderSetting'
import { useMenuSetting } from '@/hooks/setting/useMenuSetting'
import useRootSetting from '@/hooks/setting/useRootSetting'
import { Assistant } from '@/components/assistant'

function BaseLayout() {
  const { prefixCls } = useDesign('default-layout')
  const { getShowFullHeaderRef } = useHeaderSetting()
  const { getShowSidebar } = useMenuSetting()
  const { getIsMobile } = useRootSetting()

  const getLayoutClass = useDeepMemo(() => {
    return classNames([
      `${prefixCls}-out`,
      {
        // [`${prefixCls}--fixed`]: fixed,
        // [`${prefixCls}--${themeMode}`]: themeMode,
      },
    ])
  }, [prefixCls])
  return (
    <>
      <Layout className={prefixCls}>
        {getShowFullHeaderRef && <LayoutHeader fixed></LayoutHeader>}
        <Layout className={getLayoutClass}>
          {(getShowSidebar || getIsMobile) && <LayoutSider></LayoutSider>}
          <Layout className={`${prefixCls}-main`}>
            <MultipleHeader></MultipleHeader>
            <LayoutContent></LayoutContent>
            <LayoutFooter></LayoutFooter>
          </Layout>
        </Layout>
        <Assistant></Assistant>
      </Layout>
    </>
  )
}
if (process.env.NODE_ENV !== 'production') {
  BaseLayout.displayName = 'BaseLayout'
  ;(BaseLayout as any).whyDidYouRender = true
}
//export default BaseLayout
export default memo(BaseLayout)

```


