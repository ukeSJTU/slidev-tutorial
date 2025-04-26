---
layout: default
---

# 导出与托管 🚢

Slidev 提供多种导出和部署选项。

## 导出幻灯片

-   **命令:** `slidev export [entry] [options]`
-   **依赖:** 导出 PDF/PNG/PPTX 需要 `playwright-chromium` (`npm i -D playwright-chromium`)。
-   **格式:**
    -   **PDF (默认):** `slidev export`
    -   **PNG:** `slidev export --format png`
    -   **PPTX:** `slidev export --format pptx` (每页为图片，含注释)
-   **常用选项:**
    -   `--output <filename>`: 文件名。
    -   `--with-clicks`, `-c`: 为点击动画导出单独页面/图片。
    -   `--dark`: 深色主题。
    -   `--range <pages>`: 页面范围。
-   **注意:** 静态导出 (PDF, PPTX) 会丢失大部分交互功能。

---

## layout: default

# 导出与托管 🚢 (续)

## 托管幻灯片 (SPA)

将演示文稿部署为 **单页应用 (SPA)**，保留所有交互特性。

1.  **构建 SPA:**

    -   命令: `slidev build [entry] [options]`
    -   输出: `dist/` 目录。
    -   **重要:** 若部署到子目录 (如 `/my-talk/`)，需指定 `--base /my-talk/`。

2.  **部署平台:**
    -   **GitHub Pages:** 推荐使用 GitHub Actions 自动部署 (官方提供 workflow 模板)。
    -   **Netlify:** 创建 `netlify.toml` 配置文件。
    -   **Vercel:** 创建 `vercel.json` 配置文件。
    -   **Docker:** 使用预构建镜像或创建自定义 `Dockerfile`。

部署为 SPA 的核心优势是能轻松托管在任何支持静态文件的服务上。
