## 它们的作用可以用一句话来描述：就是改变`this`的指向。
## 用法`Function.call()`,`Function.apply()`,`Function.bind()`
> # 1 、call()和apply都用于*函数调用*
```ruby
function fn(){  
  alert(this) 
}

fn();//window
fn.call('hello');//'hello'
fn.apply('8888');//'8888'
```
## 区别： 
### call( thisvalue, val1，val2，….)
- thisvalue 是函数内部this的值
- 后面是参数列表
### apply( thisvalue, [val1，val2，….])
- thisvalue 是函数内部this的值
- 后面是`参数数组`，所有参数放`数组`里面

> # 2 、bind()都用于*函数创建*中
## 1、适用匿名函数
```ruby
var fn = function (a,b ){
  console.log(this,a,b);
}.bind('hello',1,2);
fn();
```
```ruby
var fn = function (a,b ){
  console.log(this,a,b);
}.bind('hello');
fn(1,2);
```
```ruby
obj.onclick = function(){

}.bind();
```

## 2、有名函数，有些特殊
```ruby
function fn(){
  console.log(this);
}
fn.bind('hello')();
```
## 3、自执行函数
```pathon
(function abc(){
  console.log(this);
}.bind('hello')());
```
```ruby
(function abc(){
  console.log(this);
}.bind('hello'))();
```
```ruby
(function abc(){
  console.log(this);
}).bind('hello')();
```
