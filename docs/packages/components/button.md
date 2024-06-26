# 按钮 ms-button

<br/>

*按钮用于开始一个即时操作*

## 何时使用

- 当需要添加一个操作按钮时

<script setup lang="ts">
import { ref } from 'vue'
const loading = ref(true)
</script>

## 基本使用

*七种类型*

<br/>

<div>
  <ms-button type="default">Default ms-button</ms-button>
  <ms-button type="primary">Primary ms-button</ms-button>
  <ms-button type="danger">Danger ms-button</ms-button>
</div>

::: details Show Code

```vue
<template>
  <div>
    <ms-button>Default ms-button</ms-button>
    <ms-button type="primary">Primary ms-button</ms-button>
    <ms-button type="danger">Danger ms-button</ms-button>
  </div>
</template>
```

:::
## APIs

参数 | 说明 | 类型 | 默认值 | 必传
-- | -- | -- | -- | --
name | 按钮文本 | string &#124; slot | '按钮' | false
type | 按钮类型 | 'default' &#124; 'primary' &#124; 'danger' &#124; 'dashed' &#124; 'text' &#124; 'link' | 'default' | false
effect | 悬浮变化效果，只有 `type` 为 `default` 时，`effect` 才生效 | 'fade' &#124; 'reverse' | 'fade' | false
size | 按钮尺寸 | 'small' &#124; 'middle' &#124; 'large' | 'middle' | false
route | 跳转目标 `URL` 地址 | {path?: string&#44; query?: object} | {} | false
target | 如何打开目标URL，设置 `route` 时生效 | '_self' &#124; '_blank' | '_self' | false
disabled | 是否禁用 | boolean | false | false
loading | 是否加载中 | boolean | false | false
center | 是否将按钮宽度调整为其父宽度并居中展示 | boolean | false | false

## Events

事件名称 | 说明 | 参数
-- | -- | --
click | 点击按钮时的回调，未设置 `route` 时生效 | (e: Event) => void
