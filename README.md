# Ld-uniapp
蓝电民间社区（非官方）uni-app 跨端应用工程，应用名：蓝友圈。

## 项目做什么

本项目基于 uni-app + Vue 3，用于构建“蓝电用户指南/社区”相关的跨端客户端，可按 uni-app 能力发布到 H5、各类小程序与 App 等平台。

- 技术栈：uni-app、Vue 3、TypeScript、Vite
- 启动页：`src/pages.json` 中的 `pages/index/index`
- 应用信息：`src/manifest.json`（名称/版本等）

## 怎么用

### 1) 安装依赖

在项目根目录执行：

```bash
npm install
```

### 2) 本地运行（开发）

H5：

```bash
npm run dev:h5
```

微信小程序：

```bash
npm run dev:mp-weixin
```

其他平台可参考 `package.json` 中的脚本（例如 `dev:mp-alipay`、`dev:mp-qq` 等）。

### 3) 构建（发布）

H5：

```bash
npm run build:h5
```

微信小程序：

```bash
npm run build:mp-weixin
```

### 4) TypeScript 类型检查

```bash
npm run type-check
```

## 目录说明（简要）

- `src/pages.json`：页面路由与导航栏配置
- `src/manifest.json`：应用名称、版本、打包配置等
- `src/pages/index/index.vue`：当前首页

## 注意事项

仓库当前包含 `unpackage/` 目录（构建产物）。如果后续希望仓库只保留源码，可再调整忽略规则；本 README 仅说明如何使用与运行。
