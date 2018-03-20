> ## 相同点：
### JavaScript 中 typeof 和 instanceof 常用来判断一个变量是否为空，或者是什么类型的。

### typeof的定义和用法：返回值是一个字符串，用来说明变量的数据类型。

> ## 细节：

- typeof 一般只能返回如下几个结果：`number`、`boolean`、`string`、`function`、`object`、`undefined`。

- typeof 来获取一个变量是否存在，如 if(typeof a!="undefined"){alert("ok")}，而不要去使用 if(a), 因为如果 a 不存在（未声明）则会出错。

- 对于 Array,Null 等特殊对象使用 typeof 一律返回 `object`，这正是 typeof 的局限性。

> ## Instanceof定义和用法：
### instanceof 用于判断一个变量是否属于某个对象的实例。

> ## 实例演示：
```ruby
a instanceof b?alert("true"):alert("false"); //a是b的实例？真:假

var a = new Array(); 
alert(a instanceof Array);  // true
alert(a instanceof Object)  // true
```
- 如上，会返回 true，同时 alert(a instanceof Object) 也会返回 true;这是因为 Array 是 object 的子类。
```ruby
function test(){};
var a = new test();
alert(a instanceof test)   // true
```
> ## 细节：

- 如下，得到的结果为‘N’,这里的 instanceof 测试的 object 是指 js 语法中的 object，不是指 dom 模型对象。
```ruby
if (window instanceof Object){ alert('Y')} else {  alert('N');}  // 'N'
```
