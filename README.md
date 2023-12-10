## 目的

`pnpm workspace` 实现 `Mono-Repo` 式项目开发结构

## 结构

web 工程是一个 Vue3 的 web 工程，components 是组件工程，utils 是工具工程
web 依赖 components 和 utils,components 依赖 utils
仅做展示用

## 附加

结合`Github Workflows`自动生成并部署到`Github Pages`

## 常用命令

添加依赖

```
#添加到根目录(-w 表示在根目录下安装依赖)
pnpm add -w vue
pnpm add -w -D vite vue-tsc typescript @vue/tsconfig @vitejs/plugin-vue @types/node @tsconfig/node18

#为子package添加依赖,(--workspace表示仅添加工作区间中的依赖)
pnpm add vue-router --filter web-demo
pnpm add ui-components --workspace --filter web-demo
```
