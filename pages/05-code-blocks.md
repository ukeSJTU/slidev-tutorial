---
layout: default
---

# 语法指南 📜: 代码块

Slidev 对代码块提供强大的支持 (使用 Shiki 高亮)。

1.  **标准围栏代码块:** 使用 ``` 加语言标识符。

    ````md
    ```typescript
    function greet(name: string) {
        console.log(`Hello, ${name}!`);
    }
    ```
    ````

2.  **导入外部代码片段 (`<<<`):** 保持 `slides.md` 整洁。

    -   语法: `<<< @/<path>[#region]{lang}{options}`
    -   `@/`: 指向项目根目录 (推荐 `@/snippets/`)。
    -   `#region-name`: 可选，导入特定 `#region`。
    -   `{lang}`: 可选，指定语言 (如 `{ts}`)。
    -   `{options}`: 可选，行高亮、Monaco 等。

    ```md
    <<< @/snippets/my-function.js
    <<< @/snippets/my-class.ts#main-logic{ts}
    <<< @/snippets/example.py{2,3|5} // 行高亮
    <<< @/snippets/config.json{json}{monaco} // Monaco 编辑器
    ```

---

## layout: default

# 代码块功能 ✨

通过在语言标识符后添加 `{}` 选项来启用高级功能：

-   **行号:** `{lines:true}`
    ```js {lines:true}
    console.log("Line 1");
    console.log("Line 2");
    ```
-   **行高亮:** `{1,3-5|7}` (支持点击逐步高亮)
    ```js {1|2}
    console.log("Highlight 1");
    console.log("Highlight 2");
    console.log("Normal");
    ```
-   **Monaco 编辑器:** `{monaco}` (可交互编辑)
    ```js {monaco}
    function hello() {
        return "Hello from Monaco!";
    }
    ```
-   **Shiki Magic Move:** 使用 ` ```magic-move ` 包裹实现代码块间平滑过渡。
-   **TwoSlash:** `{twoslash}` (TS/JS 类型提示和错误展示)。
