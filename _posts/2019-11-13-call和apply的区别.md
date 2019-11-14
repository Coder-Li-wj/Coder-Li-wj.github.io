---
layout:     post
title:      "call和apply的区别"
subtitle:   "JavaScript经典面试题"
date:       2019-11-13 09:30:00
author:     "Coder-Li-wj"
tags:
    - JavaScript
---

## call和apply的区别是什么，哪个性能更好一些？ 

### 区别：

1. call和apply都是function原型上的方法，而每一个函数作为function这个类的实例，所以可以调用原型上的call和apply方法。  
2. call和apply都是用来改变函数中this的指向，唯一的区别在于传给函数参数的方式不同，call是一个个传参，apply要求把所有参数以数组的形式传给函数。

         `fn.call(obj, 10, 20, 30)`  
         `fn.apply(obj, [10, 20, 30])`  

1. 与call和apply相类似的方法是bind，bind方法也是用来改变this的指向，但是bind并没有把函数立即执行，只是预先处理改变this。  

### 性能比较：  

call的性能要比apply好一点（尤其是传递函数的参数超过三个的时候），所以后期开发的时候可以使用call多一点。  

使用apply的情况：

```javascript
let arr = [10, 20 ,30],
    obj = {};
function fn(x, y, z) {}
fn.apply(obj, arr); //x=10,y=20,z=30
fn.call(obj, arr); //x=[10, 20, 30], y=z=undefined
fn.call(obj, ...arr); //基于ES6的展开运算符也可以实现把数组中的每一项依次传递给函数
```  

### 自己实现性能测试  

PS：但是结果只供参考，任何代码性能的测试都是和测试环境有关系的，例如CPU、内存、GPU等电脑性能，且不同浏览器也会导致性能上的不同。

测试循环十万次的方法：

```javascript
 //普通方法，不精准，循环次数少的话直接显示0
 let t1 = new Date();
 for (let i = 0; i < 100000; i++>){
   }
 console.log(new Date() - t1)

 //使用console.tme方法测试一段程序执行的时间
 console.time('A'); //A是指该次测试的名字
 for(let i = 0; i < 100000; i++>){
    }
 console.timeEnd('A')
```  

<br>  

* 另外，console.profile()在火狐浏览器中安装FireBug控制台，可以更精准的获取到程序每一个步骤所消耗的时间
