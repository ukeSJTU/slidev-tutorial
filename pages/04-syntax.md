---
layout: default
---

# 语法指南 📜: 核心

Slidev 使用扩展的 Markdown 语法。

## 幻灯片分隔符

使用三个或更多连续的连字符 `---` 并用 **空行** 包围，来分隔不同的幻灯片。

```md
# 第一张幻灯片

内容...

---

# 第二张幻灯片

更多内容...
```

---

## layout: default

# 语法指南 📜: Frontmatter

使用 YAML Frontmatter 配置幻灯片元数据和行为。

-   **Headmatter (全局):** 文件 **最顶部** 的第一个 `---` 包裹块，设置全局默认值 (主题, 标题, 默认布局等)。
-   **Frontmatter (单页):** 每个 `---` 分隔符 **之后**、内容 **之前** 的块，配置当前页特定属性 (布局, 背景, 过渡, 点击次数等)，会 **覆盖** Headmatter 中的 `defaults`。

```yaml
---
# Headmatter (全局配置)
theme: seriph
title: 我的 Slidev 演示
defaults:
    layout: default
---
# 幻灯片 1 (使用默认布局)
内容...
---
# Frontmatter (幻灯片 2 的配置)
layout: cover # 覆盖默认布局
background: /images/bg2.png
---
# 幻灯片 2
内容...
```

---

## layout: default

# 语法指南 📜: 注释 (Presenter Notes)

每张幻灯片 **末尾** 的 HTML 注释 `<!-- ... -->` 会被视为演讲者注释。

这些注释只在 **演讲者模式** 下可见，对观众隐藏。

```md
# 这是一张带注释的幻灯片

这里是幻灯片的主要内容。

<!--
这是演讲者看到的注释。
支持 Markdown 和 HTML。
-->
```
