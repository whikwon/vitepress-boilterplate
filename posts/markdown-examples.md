# Markdown content

The count is: {{ count }}

<button id="myButton" class="button" @click="count++">Increment</button>

Show Tooltip when cursor is on <span class="tooltip">here</span>.

<script setup>
import { ref, onMounted } from 'vue'
import tippy from 'tippy.js';
import 'tippy.js/dist/tippy.css';

const count = ref(0)
onMounted(() => {
  tippy(`.tooltip`, {
    content: "Hi I'm tooltip",
  });
})
</script>

<style scope>
.tooltip {
  color: blue;
}
.button {
  color: red;
  font-size: 14px;
  font-weight: bold;
}
</style>

# Markdown Extension Examples

This page demonstrates some of the built-in markdown extensions provided by VitePress.

## Syntax Highlighting

VitePress provides Syntax Highlighting powered by <span class="tooltip">[Shikiji](https://github.com/antfu/shikiji)</span>, with additional features like line-highlighting:

**Input**

````md
```js{4}
export default {
  data () {
    return {
      msg: 'Highlighted!'
    }
  }
}
```
````

**Output**

```js{4}
export default {
  data () {
    return {
      msg: 'Highlighted!'
    }
  }
}
```

## Custom Containers

**Input**

```md
::: info
This is an info box.
:::

::: tip
This is a tip.
:::

::: warning
This is a warning.
:::

::: danger
This is a dangerous warning.
:::

::: details
This is a details block.
:::
```

**Output**

::: info
This is an info box.
:::

::: tip
This is a tip.
:::

::: warning
This is a warning.
:::

::: danger
This is a dangerous warning.
:::

::: details
This is a details block.
:::

## More

Check out the documentation for the [full list of markdown extensions](https://vitepress.dev/guide/markdown).

## Math symbols

When $a \ne 0$, there are two solutions to $(ax^2 + bx + c = 0)$ and they are
$$ x = {-b \pm \sqrt{b^2-4ac} \over 2a} $$
