# 影源 · 企业智能创作平台（ai-yingyuan）

单文件、离线可用的企业智能创作 Web 应用。全部能力封装在一个 `index.html` 中，原生 HTML / CSS / JavaScript 实现，无前端框架、无后端、无构建步骤。

## 功能模块

- 企业智体中心：推荐智体、全部智体分类浏览、搜索、发布与编辑我的智体（人设、预设问题、Logo 配置、实时预览）。
- AI 写作：长篇 / 中篇 / 短篇写作、步骤化写作向导（10 大类、116 个公文场景级联）、智能续写、内容润色、文本校对、历史记录。
- 我的智体编排：自定义智体的创建、编辑、调试预览与管理。
- 探文智述：文档库管理、PDF / Word / TXT 上传与文本提取、基于原文的文档问答（回答附依据）。
- AI 文档：一键分析、关键词提取、摘要与结构化结论。
- 公文范文库：14 篇分类范文、详情阅读、一键套用进编辑器。
- 小影 AI：多轮对话、意图识别、会话管理、模型切换、流式输出。

## 技术特点

- 单文件交付，双击 `index.html` 即可在浏览器离线运行。
- hash 路由，localStorage 本地持久化（键 `yingyuan_proto_v1`），不上传任何用户数据。
- 规则化 AI 引擎 + 流式打字机输出，无外部 API 依赖。
- 图标全部为手写内联 SVG，未使用 emoji 与图标字体。

## 运行方式

1. 直接运行：下载 `index.html`，用现代浏览器（Chrome / Edge / Firefox）打开即可。
2. 本地服务：
   ```bash
   # 任选其一
   python3 -m http.server 8080
   npx serve .
   ```
   浏览器访问 http://localhost:8080 。
3. GitHub Pages 在线访问：仓库 Settings → Pages → Source 选择 `main` 分支、根目录 `/ (root)`，保存后等待约 1 分钟，通过 Pages 提供的网址访问。

## 目录说明

- `index.html`：完整应用（唯一运行文件）。
- `.github/workflows/merge.yml`：发布工作流（从校验过的单一来源生成 index.html）。
- `SHA256SUMS`：已发布 `index.html` 的 SHA-256 校验值。
