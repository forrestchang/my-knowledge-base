## 一、创建一个 Vue 实例

```javascript
var vm = new Vue({ // vm -> ViewModel
	// 选项
})
```

一个 Vue 应用由一个通过 `new Vue` 创建的根 Vue 实例，以及可选的嵌套的，可复用的组件树构成。

## 二、数据与方法

当一个 Vue 实例被创建时，它向 Vue 的响应式系统中加入了其 `data` 对象中能找到的所有的属性。当 `data` 中的数据改变时，视图会进行重新渲染。

注：只有当实例被创建时 `data` 中存在的属性才是响应式的，如果后来新添加一个新的属性，那么改动将不会触发任何视图的更新。可以通过设置初始值的办法来解决。

Vue 实例暴露的一些有用的实例属性与方法：

- vm.$data // -> data
- vm.$el  // -> document.getElementById('example')
- vm.$watch

	```
	vm.$watch('a', function(newValue, oldValue){})  // 这个回调将会在 `vm.a` 改变后调用
	```

## 三、实例声明周期钩子

created, mounted, updated, destroyed 等。

不要在选项属性或回调上使用箭头函数，例如 `created:() => console.log(this.s)` 或 `vm.$watch('a', newValue => this.myMethon())`。因为箭头函数式和父级上下文绑定在一起的，`this` 不会是如你所预期的 Vue 实例。

## 四、声明周期图示

![](https://cn.vuejs.org/images/lifecycle.png)


