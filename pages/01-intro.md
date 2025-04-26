---
layout: default
---

# 为什么选择 Slidev？ 🤔

Slidev 专为开发者设计，旨在提供一种既简单又强大的演示文稿创建方式。

-   **📝 基于 Markdown:** 扩展 Markdown 格式，便于版本控制和编辑。
-   **🧑‍💻 开发者友好:** 一流的代码片段支持，精确语法高亮 (Shiki)。
-   **🎨 可定制主题:** 通过 npm 包轻松切换主题。
-   **⚡️ 快速:** 基于 Vite，实现即时预览更新 (HMR)。
-   **🤹 交互性与表现力:** 嵌入 Vue 组件，实现丰富交互。
-   **✨ 渐进式:** 从简单 Markdown 开始，逐步引入功能。
-   **🎥 录制支持:** 内置录制和摄像头视图。
-   **📤 便携性:** 导出为 PDF、PNG、PPTX 或 SPA。
-   **🛠️ 可扩展与 Hackable:** 基于 Web 技术，高度可定制。

---

## layout: default

# 基础使用 🚀

开始使用 Slidev 非常简单。

1.  **环境要求:** Node.js 18.0 或更高版本。
2.  **创建项目:** (推荐使用 pnpm)
    ```bash
    pnpm create slidev
    # 或 npm init slidev@latest
    # 或 yarn create slidev
    # 或 bun create slidev
    ```
3.  **核心文件:** `slides.md` (包含你的幻灯片内容)。
4.  **启动开发服务器:**
    ```bash
    cd your-slidev-project
    pnpm run dev # 或 npm run dev / yarn dev / bun run dev
    ```
5.  **在线尝试:** 访问 [sli.dev/new](https://sli.dev/new) 直接在浏览器中体验。
