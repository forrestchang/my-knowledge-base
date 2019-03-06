CSS: x-devonthink-item://A40585BB-938F-40CC-B971-C671F64F738C

<head>
  <script type="text/javascript" async
    src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
  </script>
</head>

必须把 `v-if` 作用到一个元素上，如果想切换多个元素的话，可以使用 `<template>` 元素当做不可见的包裹元素，并在上面使用 `v-if`。

`v-else` 使用 else 块。

`v-else-if` 使用 else if 块。

`v-show` 不支持 `<template>` 标签。

`v-if` 与 `v-for` 一起使用时，`v-for` 具有比 `v-if` 更高的优先级。