# el与data的两种写法

## el的两种写法

1. new Vue时配置el属性

   ```javascript
   new Vue({
       el:'#root',
   })
   ```

2. 先创建Vue实例，随后再通过`vm.$mount('#root')`指定el的值

   ```javascript
   const vm = new Vue({
       data() {
           return {
               name:'xiaolong'
           }
       }
   })
   vm.$mount('#root')
   ```

   

## data的两种写法

1. 对象式

   ```javascript
   new Vue({
       data: {
           name: 'xiaolong'
       }
   })
   ```

   

2. 函数式

   如何选择：目前那种方式写都可以，以后学到组件时，data必须用函数式，否则会报错

   ```javascript
   new Vue({
       data() {
           return {
               name: 'xiaolong'
           }
       }
   })

## 一个重要的原则

由Vue管理的函数，一定不要写箭头函数，一旦写了箭头函数，`this`就不是Vue实例了