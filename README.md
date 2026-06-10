# Sunny AI

一个面向 AI 发布工作流的个人富 UI 内容网站。

目标是让你以后只需要说：

> 保存到我的网站 `/guides/xxx`

AI 就可以生成一个富 UI 页面，写入 `src/pages/...`，由 Cloudflare Pages / Vercel 自动部署并返回链接。

## 技术栈

- Astro 静态网站
- 组件化 `.astro` 页面
- 不以 Markdown 为主要内容格式
- 适合富 UI 长文、专题页、技术报告、分享页
- GitHub 仓库作为 AI 可写入的内容库

## 本地启动

```bash
npm install
npm run dev
```

## 构建

```bash
npm run build
npm run preview
```

## 推荐部署

### Cloudflare Pages

- Build command: `npm run build`
- Output directory: `dist`

### Vercel

直接导入 GitHub 仓库，Framework 选择 Astro。

## 目录约定

```text
src/pages/guides/      正式专题页
src/pages/posts/       普通文章页
src/pages/drafts/      草稿页
src/components/        可复用 UI 组件
src/layouts/           页面布局
src/styles/global.css  全局样式
content-protocol.md    给 AI 使用的发布协议
```

## AI 发布指令示例

```text
把这篇文章保存到我的网站：
路径 /guides/loop-engineering
标题《Loop Engineering 入门》
风格：解释型专题页，UI 丰富
状态：公开发布
```

AI 应写入：

```text
src/pages/guides/loop-engineering.astro
```

最终链接：

```text
https://你的域名/guides/loop-engineering
```

## Deployment note

Cloudflare Pages should build from the latest commit on the default branch.
