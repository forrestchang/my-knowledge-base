CSS: x-devonthink-item://A40585BB-938F-40CC-B971-C671F64F738C

<head>
  <script type="text/javascript" async
    src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
  </script>
</head>

在底层的实现上，Vue 将模板编译成虚拟 DOM 渲染函数，结合响应系统，Vue 能够智能地计算出最少需要重新渲染多少组件，并把 DOM 操作次数减到最小。

## 插值

### 文本

```
{{ message }}

<p v-once>{{ test }}</p>
```

使用 `v-once` 只能够执行一次插值，之后 `test` 改变不会重新更新。

### 原始 HTML

使用 `v-html`。

### JavaScript

```
{{  message.split(',').reverse().join('') }}
```

模板表达式都被放在沙盒中，智能访问全局变量的一个白名单，例如 Date 或者 Math。

## 指令

指令的职责是，当表达式的值改变时，将其产生的连带影响，响应式地作用于 DOM。

### 参数

一些指令能够接收一个参数，在指令名称之后以冒号表示：`v-bind:href`，`v-on:click="something"`。

2.6.0 新增动态参数

```
<a v-on:[eventName]="doSomething"></a>
```

动态参数是一个字符串，非字符串会触发警告。

### 修饰符

修饰符（modifier）是以半角句号 `.` 指明的特殊后缀，用于支出一个指令应该以特殊方式绑定，例如 `.prevent` 修饰符告诉 `v-on` 指令对于触发的事件调用 `event.preventDefault()`：

```
<form v-on:submit.prevent="onSubmit"></form>
```

## 缩写

- `v-bind:href` => `:href`
- `v-on:click` => `@click`

