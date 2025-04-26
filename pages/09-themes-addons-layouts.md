---
layout: default
---

# 定制化: 主题 (Themes) 🎨

主题主要负责演示文稿的 **视觉外观**。

-   **作用:** 全局样式、字体、颜色方案，并可提供自定义布局和组件。
-   **使用:**
    1.  在 Headmatter 中指定 `theme: <theme-name>` 或 `theme: ./path/to/local/theme`。
    2.  Slidev 会提示自动安装 (或手动 `npm i slidev-theme-<name>`)。
-   **编写:**
    -   使用 `pnpm create slidev-theme` 创建模板。
    -   添加样式 (`style.css`), 布局 (`layouts/`), 组件 (`components/`)。
    -   在 `package.json` 中设置默认配置 (`slidev.defaults`) 和元数据。
    -   通过 `theme: ./` 在本地预览。
-   **发布:** 包名 `slidev-theme-<name>`, 关键词 `slidev-theme`, `slidev`。

---

## layout: default

# 定制化: 插件 (Addons) 🧩

插件主要用于添加 **功能性** 扩展。

-   **作用:** 图标集、绘图工具、代码运行器、特定组件库集成等。
-   **与主题区别:** 主题管"皮肤"，插件管"功能"。
-   **使用:**
    1.  在 Headmatter 的 `addons` 数组中列出插件名或路径。
    2.  安装方式与主题类似。
-   **编写:**
    -   结构类似主题，包含 `components/`, `layouts/`, `setup/` 等。
    -   侧重于添加新功能，避免覆盖性样式。
    -   通过 `addons: ['./']` 在本地预览。
-   **发布:** 包名 `slidev-addon-<name>`, 关键词 `slidev-addon`, `slidev`。

---

## layout: default

# 定制化: 布局 (Layouts) 🖼️

布局定义幻灯片内容的 **结构和框架** (本质是 Vue 组件)。

-   **使用:**
    1.  在单页 Frontmatter 中指定 `layout: <layout-name>`。
    2.  默认: 第一页 `cover`, 其余 `default`。
    3.  加载顺序 (同名覆盖): 内置 -> 主题 -> 插件 -> 项目本地 (`layouts/`)。
-   **编写:**

    1.  在项目根目录 `layouts/` 下创建 Vue 文件 (如 `TwoCols.vue`)。
    2.  使用 `<slot/>` 指定 Markdown 内容插入位置。
    3.  使用 **命名插槽** (`<slot name="xxx"/>`) 定义多个内容区。

    ```vue
    <!-- layouts/TwoCols.vue -->
    <template>
        <div class="grid grid-cols-2 gap-4">
            <div><slot /></div>
            <!-- 默认插槽 -->
            <div><slot name="right" /></div>
            <!-- 命名插槽 -->
        </div>
    </template>
    ```

    ```md
    ---
    layout: two-cols
    ---

    这是左边的内容 (默认插槽)。

    ::right::

    这是右边的内容 (命名插槽 `right`)。
    ```

</rewritten_file>
