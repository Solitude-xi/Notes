# 初始Vue

1. 想要`Vue`工作，就必须创建一个`Vue`实例，且要传入一个配置对象

2. root容器里的代码依然符合`html`规范,，只不过混入了一些特殊的`Vue`语法

3. root容器里的代码成为【Vue模板】

4. `Vue`实例和容器是一一对应的

5. 真实开发中只有一个`Vue`实例，并且会配合着组件一起使用

6. `{{xxx}}`中的xxx要写JS表达式，且xxx可以自动读取到data中的所有属性

7. 一旦data中的数据发生改变，那么模板中用到改数据的地方也就会自动更新

   ## 注意区分：JS表达式和JS代码（语句）

   1. 表达式：一个表达式会产生一个值，可以放到任何一个需要值的地方
      - a
      - a + b
      - demo(1)
      - x === y ? 'a', 'b'
   2. JS代码（语句）
      - `if () {}`
      - `for () {}`

```html
<div id='root'>
    <h1>
        hello, {{name}}
    </h1>
</div>
```

```javascript
new Vue({
    el:'#root',
    data: {
        name:'w'
    }
})
```



