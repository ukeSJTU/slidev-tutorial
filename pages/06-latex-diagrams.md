---
layout: default
---

# 语法指南 📜: LaTeX (数学公式)

Slidev 内置 KaTeX 支持 LaTeX 数学和化学公式渲染。

-   **行内模式:** 使用单个美元符号 `$` 包裹。

    这是一个行内公式 $E = mc^2$。

-   **块模式:** 使用双美元符号 `$$` 包裹，公式居中显示。

    $$
    \frac{\partial \rho}{\partial t} + \nabla \cdot (\rho \mathbf{v}) = 0
    $$

-   **行高亮:** 块模式支持 `{}` 高亮行号 (从 1 开始)。

    $$
    {1|3}
    L = \frac{1}{2} \rho v^2 S C_L
    $$

-   **化学方程式 (`mhchem`):** 需要额外配置 (见配置部分)，使用 `\ce{...}`。

    $$\ce{H2 + O2 -> H2O}$$

-   **图表 (Diagrams):** Slidev 也支持 Mermaid 和 PlantUML 图表 (详见文档)。

    ```mermaid
    graph TD
        A[Start] --> B{Is it?};
        B -- Yes --> C[OK];
        C --> D[End];
        B -- No --> E[Fix it];
        E --> B;
    ```
