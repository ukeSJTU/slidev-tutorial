---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# some information about your slides (markdown enabled)
title: Slidev 教程
info: |
  一个基于 CONTRIBUTING.md 的 Slidev 快速入门教程。

  按 Space 或 → 继续。
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# open graph
# seoMeta:
#  ogImage: https://cover.sli.dev
---

# Slidev 教程

一个为开发者准备的幻灯片制作工具

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    开始学习 <carbon:arrow-right/>
  </span>
</div>

<!--
这是第一页的注释
-->

---
src: ./pages/01-intro.md
---

---
src: ./pages/02-cli-project.md
---

---
src: ./pages/03-editor.md
---

---
src: ./pages/04-syntax.md
---

---
src: ./pages/05-code-blocks.md
---

---
src: ./pages/06-latex-diagrams.md
---

---
src: ./pages/07-customization-intro.md
---

---
src: ./pages/08-config-files.md
---

---
src: ./pages/09-themes-addons-layouts.md
---

---
src: ./pages/10-global-context.md
---

---
src: ./pages/11-export-hosting.md
---

---
src: ./pages/12-components.md
---

---
src: ./pages/13-animations.md
---

---
src: ./pages/14-conclusion.md
---