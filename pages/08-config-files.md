---
layout: default
---

# 定制化: `setup/` & `vite.config.ts` ⚙️

深入配置内部工具。

-   **`./setup/shiki.ts`**: 配置 Shiki 语法高亮器。

    -   指定亮/暗主题 (`themes`)。
    -   添加额外语言支持 (`langs`)。

    ```ts
    // ./setup/shiki.ts
    import { defineShikiSetup } from "@slidev/types";
    export default defineShikiSetup(() => ({
        themes: {
            dark: "min-dark",
            light: "min-light",
        },
    }));
    ```

-   **`./setup/katex.ts`**: 配置 KaTeX 渲染引擎。
    -   传递 KaTeX 选项 (如 `macros`)。
    ```ts
    // ./setup/katex.ts
    import { defineKatexSetup } from "@slidev/types";
    export default defineKatexSetup(() => ({
        macros: { "\\RR": "\\mathbb{R}" },
    }));
    ```

---

## layout: default

# 定制化: `setup/` & `vite.config.ts` (续)

-   **`./setup/monaco.ts`**: 配置 Monaco 编辑器。

    -   设置编辑器选项 (`editorOptions`)。
    -   配置 TypeScript 类型加载。
    -   **注意:** Monaco 主题会自动跟随 Shiki 配置。

    ```ts
    // ./setup/monaco.ts
    import { defineMonacoSetup } from "@slidev/types";
    export default defineMonacoSetup(async (monaco) => {
        return {
            editorOptions: { fontSize: 14 },
        };
    });
    ```

-   **`vite.config.ts`** (根目录): 扩展或覆盖 Vite 配置。

    -   添加自定义 Vite 插件。
    -   **高级:** 通过 `slidev` 字段配置内部 Vite 插件 (谨慎使用)。

    ```ts
    // vite.config.ts
    import { defineConfig } from "vite";
    export default defineConfig({
        // 添加自定义插件
        // plugins: [MyCustomPlugin()],
    });
    ```

-   **其他 `setup/` 文件:** `main.ts` (Vue App), `unocss.ts`, `code-runners.ts` 等 (详见文档)。
