```ruby
var oBox = document.getElementById("box");
console.log(oBox.style.width);
```

- **oBox.style.width 只能`获取`或者`修改`行内样式**
 
```ruby
  function getStyle( obj , attr ){
    return window.getComputedStyle ? getComputedStyle(obj)[attr] : obj.currentStyle[attr];
  }
 ```
 
 - **通过 getComputedStyle() 方法获取style标签外联样式**
 - **在 IE8 以下使用 currentStyle()**
