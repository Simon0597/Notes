> # Events in JavaScript [mouse events, keyboard events, form events, system events]
- onclick —————— 点击（单击）事件 
- onmouseover ———– 鼠标滑入事件（会冒泡） 
- onmouseout—————鼠标离开事件（会冒泡） 
- onmouseenter————鼠标滑入事件（不会冒泡） 
- onmouseleave————鼠标离开事件（不会冒泡） 
- ondblclick ——————- 双击（单击）事件
## 如果传入一个函数是被事件调用的,那么这个函数定义的第一个参数就是事件对象
  **ie:** event是一个内置全局对象
```ruby
  var  obj.onclick = function(ev){
    var ev = ev || window.event;
  }
  function abc(ev){
    var ev = ev || window.event;
  }
```

:+1: 更多参考[W3School](http://www.w3school.com.cn/tags/html_ref_eventattributes.asp)

> # Bubble（冒泡）
**事件冒泡指子元素触发事件的时候，会冒泡（触发）`父级`的相同的事件**
### 阻止冒泡：
- 非标准：ev.stopPopagation(); 
- 非标准：ev.cancelBubble=true; **ie9以下也支持**
```rudy
  if(e.stopPropagation){
    e.stopPropagation()
  }else{
    cancelBubble = true;
  }
```
 > # 注册处理事件
 **如果有多个相同事件，将采用此方法进行添加事件**
 ## 1、标准：obj.addEventListener(事件名称，事件函数，是否捕获);
.addEventListener("click",function(){},false)  **//false指不捕获（捕获是父到子，冒泡是子到父）先捕获后冒泡，当前元素有捕获也有冒泡，按照执行顺序在前的先执行**

**是否捕获**
- false冒泡 
- true捕获

**先捕获后冒泡**
- 有捕获 
- 事件名称没有on 
- 事件执行的顺序是正序 
- this触发该事件的对象

## 2、低版ie：obj.attachEvent(事件名称，事件函数);
- 没有捕获 
- 事件名称有on 
- 事件函数执行的顺序：标准ie-》正序 非标准ie-》倒序 
- this指向window

## 3、 移除 obj.removeEventListener(事件名称，事件函数)

## 4、 移除 object.detachEvent(事件名称,function);
