CSS: x-devonthink-item://A40585BB-938F-40CC-B971-C671F64F738C

<head>
  <script type="text/javascript" async
    src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
  </script>
</head>

`v-for` 支持一个可选的第二个参数作为当前的索引：

```
<li v-for="(item, index) in items"></li>
```

遍历对象：

```
<div v-for="(value, key, index) in object">
{{ index }}. {{ key }}: {{ value }}
</div>
```

---

