# Vue.js学习
---
>官方教程地址：https://cn.vuejs.org/v2/guide/index.html

1. 实例化Vue
```
var vm = new Vue({
	//选项
})
```

2. 文本插值
```
<span>Message: {{ message }}</span>

var app = new Vue({
				el:'#app',
				data:{
					message:'hello vue!'
				}
			})
```

3. data的json数据定义
	* 标准的json数据，
	* 注意数组与非数组时的符号使用[],{}

4. for循环
* 我们用 v-for 指令根据一组数组的选项列表进行渲染。v-for 指令需要使用 item in items 形式的特殊语法，items 是源数据数组并且 item 是数组元素迭代的别名。
```
<ul id="example-1">
  <li v-for="item in items">
    {{ item.message }}
  </li>
</ul>
var example1 = new Vue({
  el: '#example-1',
  data: {
    items: [
      { message: 'Foo' },
      { message: 'Bar' }
    ]
  }
})
```
* 一个对象的v-for
```
<ul id="v-for-object" class="demo">
  <li v-for="value in object">
    {{ value }}
  </li>
</ul>
new Vue({
  el: '#v-for-object',
  data: {
    object: {
      firstName: 'John',
      lastName: 'Doe',
      age: 30
    }
  }
})
```
