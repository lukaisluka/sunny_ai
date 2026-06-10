# AI Publishing Protocol

这个文件定义 AI 往网站写文章时必须遵守的规则。

## 1. 内容形态

不要生成 Markdown 文章。默认生成 `.astro` 页面。

## 2. 页面路径

- 正式专题页：`src/pages/guides/<slug>.astro`
- 普通文章：`src/pages/posts/<slug>.astro`
- 草稿：`src/pages/drafts/<slug>.astro`

## 3. 页面必须包含

每个页面都应该包含：

- `Layout`
- `Hero`
- 至少 3 个结构化 section
- 一个 `SummaryCard` 或 `Callout`
- 一个 `FAQ`，除非用户明确不需要
- SEO title / description

## 4. 推荐组件

- `Hero`
- `Section`
- `Callout`
- `FeatureGrid`
- `StepTimeline`
- `Comparison`
- `RiskGrid`
- `Checklist`
- `FAQ`
- `CodePanel`

## 5. 写作风格

- 中文为主
- 概念解释要由浅入深
- 不要堆砌术语
- 适合分享给非上下文读者
- 保留工程判断和风险边界

## 6. 发布安全规则

AI 不应自动发布以下内容，除非用户明确确认：

- 密钥、token、账号、私有链接
- 公司内部敏感信息
- 未确认的投资建议
- 法律、医疗、合规结论
- 生产事故细节
- 未脱敏日志

## 7. 推荐命令约定

用户说：

```text
保存到网站
```

默认保存为草稿。

用户说：

```text
发布到网站
```

保存到公开页面目录。

用户说：

```text
更新网站上的 xxx
```

先读取现有页面，再修改，不要覆盖未知内容。
