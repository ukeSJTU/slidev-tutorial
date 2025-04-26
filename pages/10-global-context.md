---
layout: default
---

# 全局上下文 🌍

Slidev 向每个幻灯片和组件注入一个"全局上下文"，包含响应式状态和控制函数，用于动态访问和操作演示状态。

**访问方式:**

1.  **模板内 (`$` 前缀):**
    -   Markdown: `当前页码: {{ $nav.currentPage }}`
    -   Vue 模板: `<button @click="$nav.nextSlide()">下一页</button>`
2.  **组合式 API (Composable):** 在 `<script setup>` 中导入。
    ```ts
    import { useNav } from "@slidev/client";
    const { currentPage, next } = useNav();
    ```

---

## layout: default

# 全局上下文: 关键属性 ✨

-   **`$slidev`**: 主上下文对象 (包含配置 `configs`, 主题配置 `themeConfigs` 等)。
-   **`$nav`**: 响应式导航对象。
    -   `$nav.currentPage`: 当前页码 (从 1 开始)。
    -   `$nav.currentLayout`: 当前布局。
    -   `$nav.clicks`: **全局**点击计数。
    -   `$nav.next()`, `$nav.prev()`, `$nav.go(index)`, `$nav.nextSlide()`, `$nav.prevSlide()`: 导航函数。
-   **`$frontmatter`**: 当前幻灯片的 Frontmatter。
-   **`$clicks`**: 当前幻灯片**内部**的点击计数 (从 0 开始)。
-   **`$page`**: `$nav.currentPage` 的别名。
-   **`$renderContext`**: 渲染环境 (`'slide'`, `'overview'`, `'presenter'`, `'print'` 等)。

**Composable 函数:**
`useNav()`, `useSlideContext()`, `useDarkMode()`, `useClicks()`, `useSlideInfo()`, `useIsSlideActive()`, `onSlideEnter()`, `onSlideLeave()` 等。
