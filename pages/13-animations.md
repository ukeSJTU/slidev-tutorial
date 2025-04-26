---
layout: default
---

# 动画 (Animations) ✨

为演示文稿添加动态效果。

## 点击动画 (Click Animations)

元素根据用户点击（或按键）逐步显示/隐藏。

-   **`v-click` / `<v-click>`:** 基础指令/组件，使元素初始隐藏，下次点击显示。
    ```md
    <div v-click>Step 1</div>
    <v-click>Step 2</v-click>
    ```
-   **`v-after` / `<v-after>`:** 与 **前一个** `v-click` **同时** 出现。
    ```md
    <div v-click>Hello</div>
    <div v-after>World</div> <!-- Hello 和 World 同时出现 -->
    ```
-   **隐藏 (`.hide` / `hide` prop):** 后续点击隐藏元素。
    ```md
    <div v-click.hide>出现后再次点击隐藏</div>
    ```
-   **`v-clicks` / `<v-clicks>`:** 自动为子元素应用 `v-click` (常用语列表)。
    ```md
    <ul v-clicks>
      <li>Item 1</li>
      <li>Item 2</li>
    </ul>
    ```

---

## layout: default

# 动画 (Animations) ✨ (续)

## 点击动画控制

-   **指定索引:**
    -   绝对定位: `v-click="3"` (第 3 次点击出现)
    -   相对定位: `v-click="+2"` (在上一个相对定位点击索引 +2 时出现)
-   **范围 (`v-click="[enter, leave]"`):** 控制元素显示和隐藏的点击范围。
    ```md
    <div v-click="[2, 5]">在第 2 次点击出现，第 5 次点击消失</div>
    ```
-   **`<v-switch>`:** 基于模板的更灵活的范围控制。
-   **自定义总点击数:** Frontmatter 中 `clicks: <number>`。
-   **过渡效果:** 默认有透明度过渡。可自定义 CSS 类 (`.slidev-vclick-target`, `.slidev-vclick-hidden`) 实现复杂动画。

## 幻灯片过渡 (Slide Transitions)

切换幻灯片时的效果。

-   **设置:** Headmatter 或单页 Frontmatter `transition: <name>`。
-   **效果:** `fade`, `fade-out`, `slide-left`, `slide-right`, `slide-up`, `slide-down`, `view-transition` (实验性)。
-   **方向:** `transition: slide-left | slide-right` (前进 | 后退)。
-   **自定义:** 定义 Vue 过渡类并使用。

## Motion (`v-motion`)

集成 `@vueuse/motion`，实现更复杂的单元素动画 (详见文档)。
