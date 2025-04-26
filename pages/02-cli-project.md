---
layout: default
---

# 命令行工具 (CLI) 💻

Slidev 提供了一套 CLI 工具来管理演示文稿。

-   **`slidev [entry]` (或 `slidev dev [entry]`)**: 启动本地开发服务器。

    -   `--port <port>`: 指定端口 (默认 3030)。
    -   `--open`, `-o`: 自动打开浏览器。
    -   `--theme <theme>`: 临时切换主题预览。

-   **`slidev build [entry]`**: 构建用于部署的 SPA (单页应用)。

    -   `--out <dir>`: 指定输出目录 (默认 `dist`)。
    -   `--base <path>`: 设置部署的基础 URL。
    -   `--download`: 在 SPA 中启用 PDF 下载。

-   **`slidev export [entry]`**: 导出为不同格式 (PDF, PNG, PPTX)。

    -   `--format <format>`: 指定格式 (默认 `pdf`)。
    -   `--output <filename>`: 指定文件名。
    -   `--dark`: 使用深色主题。
    -   `--with-clicks`: 为点击动画导出单独页面/图片。

-   **`slidev theme eject [entry]`**: 提取主题文件进行定制。

-   **`slidev --help`**: 显示帮助信息。

---

## layout: default

# 项目结构 📁

Slidev 项目遵循约定结构，核心是 `slides.md`。

```text
your-slidev/
├── components/     # (可选) 自定义 Vue 组件
├── layouts/        # (可选) 自定义布局
├── public/         # (可选) 静态资源 (图片、字体等)
├── setup/          # (可选) 高级配置 (shiki, katex, vite)
├── snippets/       # (可选) 代码片段 (用于 <<< 导入)
├── styles/         # (可选) 自定义样式
├── index.html      # (可选) 注入 Meta 或脚本
├── slides.md       # (必需) 幻灯片主文件
├── vite.config.ts  # (可选) 扩展 Vite 配置
└── package.json    # 项目依赖和脚本
```

大部分目录和文件都是可选的，按需创建。
