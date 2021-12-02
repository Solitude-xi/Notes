# MVVM模型

1. M：模型（Model）：data中的数据
2. V：视图（View）：模板代码
3. VM：视图模型（ViewModel）：Vue实例

## 观察发现

1. data中的所有属性，最后都出现在了vm上
2. vm身上的所有属性，以及Vue原型上的所有属性，在Vue模板中都可以直接使用