CSS: x-devonthink-item://A40585BB-938F-40CC-B971-C671F64F738C

<head>
  <script type="text/javascript" async
    src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
  </script>
</head>

## 绑定 HTML Class

### 对象语法

我们可以传给 `v-bind:class` 一个对象，以动态地切换 class：

```
<div v-bind:class="{active: isActive}"></div>
```

上面的语法表示 `active` 这个 class 的存在与否将取决于数据属性 `isActive` 的真值。

更强大的使用方法，绑定一个计算属性：

```
<div v-bind:class="classObj"></div>

data: {
	isActive: true,
	error: null
},

computed: {
	classObj() {
		return {
			active: this.isActive && !this.error,
			'text-danger': this.error && this.error.type === 'fatal'
		}
	}
}
```

## 绑定内联样式

和绑定 class 的用法相同。

