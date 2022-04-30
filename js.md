### JS对象基本用法
#### 1. 声明对象的两种语法
+  第一种：
```JavaScript
let obj = new Object{}
```
+  第二种：
```JavaScript
let obj = {}
```
#### 2. 删除对象的属性
语法
```javascript
delete obj.property
delete obj['property']
```
```javascript
let Employee = {
  age: 28,
  name: 'jack',
  designation: 'developer'
}
```
+ 删除对象属性的值
```javascript
obj.name = undefined
````
+ 删除对象名连同值
```javascript
delete obj.name
或delete obj['name']
```
#### 查看对象的属性
+ Object.keys(obj)  
遍历对象，返回对象中可枚举的键的字符串数组
+ Object.value(obj)  
打印obj的属性值
+ Object.entries(obj)  
打印属性和属性值
+ console.dir(obj)  
打印出该对象的所有属性和属性值
+ boj.hasOwnProperty('property')  
判断一个属性是自身的或者是共有的
#### 修改或增加对象的属性
+ 直接赋值  
```javascript
let Employee = {name: 'jack'}  
```
如果该对象中有此属性，它就修改属性的值，如果没有它就自动添加
+ 批量赋值  
```javascript
Object.assign(obj, {age: 18, gender: 'man'})
```
#### 'name' in obj和obj.hasOwnProperty('name') 的区别
'name' in obj无法判断该属性是自身的或是共有的  
obj.hasOwnProperty('name')可以断定该属性是否为自身的
