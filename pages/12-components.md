---
layout: default
---

# 组件 (Components) 🧩

直接在 Markdown 中使用 Vue 组件，无需导入！

## 使用内置组件

Slidev 提供了一系列开箱即用的组件。

```md
<!-- 嵌入推文 -->
<Tweet id="1390115482657726468" />

<!-- 嵌入 YouTube 视频 -->
<Youtube id="dQw4w9WgXcQ" />

<!-- 根据亮/暗模式显示不同内容 -->
<LightOrDark>
  <template #dark>⚫️ Dark mode content</template>
  <template #light>⚪️ Light mode content</template>
</LightOrDark>

<!-- 生成目录 -->
<Toc maxDepth="2" />
```

**参考:** 完整列表请查阅 [内置组件文档](https://sli.dev/builtin/components)。

---

## layout: default

# 组件 (Components) 🧩 (续)

## 使用自定义组件

创建自己的 Vue 组件并在 Slidev 中复用。

1.  **创建组件:** 在 `./components/` 目录下创建 `.vue` 文件 (如 `MyCounter.vue`)。

    ```vue
    <!-- components/MyCounter.vue -->
    <script setup>
    import { ref } from "vue";
    const count = ref(0);
    </script>
    <template>
        <button @click="count++">Count: {{ count }}</button>
    </template>
    ```

2.  **使用组件:** 在 `slides.md` 中直接使用组件名 (驼峰或短横线)。

    ```md
    # 自定义组件示例

    <MyCounter />
    <my-counter />
    ```

3.  **主题/插件组件:** 主题和插件也可以提供组件，使用方式相同。

这使得你可以利用整个 Vue 生态系统来创建丰富的交互式幻灯片！
