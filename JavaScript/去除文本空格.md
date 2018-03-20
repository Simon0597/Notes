> # 方法一：使用replace正则匹配的方法

去除所有空格: str = str.replace(/\s*/g,"");      

去除两头空格: str = str.replace(/^\s*|\s*$/g,"");

去除左空格： str = str.replace( /^\s*/, “”);

去除右空格： str = str.replace(/(\s*$)/g, "");

### str为要去除空格的字符串，实例如下：
```ruby
var str = " 23 23 ";
var str2 = str.replace(/\s*/g,"");
console.log(str2); // 2323
```
> # 方法二：使用str.trim()方法

### str.trim()局限性：无法去除中间的空格，实例如下：
```ruby
var str = "   xiao  ming   ";
var str2 = str.trim();
console.log(str2);   //xiao  ming 
```
### 同理，str.trimLeft()，str.trimRight()分别用于去除字符串左右空格。
