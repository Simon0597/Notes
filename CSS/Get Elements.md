- 通过ID名字获取元素  document.getElementById("box");
- 通过ClassName获取元素 document.getElementsByClassName("ClassName")
- 通过  Name 获取元素 document.getElementsByName("Name") *一般用于表单元素*
- 通过标签名字获取元素  document.getElementsByTagName("TagName")

>下面两个方法，括号里的东西符合CSS规则
- document.querySelector()  *选择一个*
- document.querySelectorAll() *选择多个*
 
>特殊的标签
- document.body
- document.head
- document.title

:exclamation: **需要注意的事项**：
    除了特殊标签以及ID获取，其他的可以把document换成一个**元素**

- document.getElementById() 匹配ID名称...
- ele.getElementsByTagName() 匹配标签名是...的集合动态方法
- document.getElementsByName() 匹配name是...的集合 动态方法
- ele.getElementsByClassName() 匹配class名称...的集合 动态方法
- ele.querySelector(); 匹配css选择器的第一个
- ele.querySelectorAll(); 匹配css选择器匹配的所有集合 
  . 及[]的运用
      
```python
	<div id="big">1
		<div class="small">2</div>
	</div>
	<div class="small2">3</div>

	<script type="text/javascript">
		var bigDiv = document.getElementById("big"),
		smallDiv = bigDiv.getElementsByClassName("small"),
		smallDiv2 = bigDiv.getElementsByClassName("small2");
		console.log(smallDiv)
		console.log(smallDiv2)
	</script>
```        
 **以上的smallDiv打印出来的是 HTMLCollection [div.small] 而smallDiv2打印出来的是 HTMLCollection []**
> ## innerHTML , innerText , textContent
- 三者都是获取元素内部的文字内容
- console.log( ele.innerText );	//`不可以`获取隐藏元素的文字内容
- console.log( ele.textContent );	//`可以`获取隐藏元素的文字内容

# :exclamation:注意
获取类名属性，要加**下标**，比如var demo1 = document.getElementsByClassName("demo1")**[0]**;
> id 就像桌上的一个苹果，拿着就可以吃，class 就像桌上一个箱子，箱子里有一个苹果，虽然只有一个，但从桌子上获取到的是箱子，而不能直接获取到箱子里的苹果，所以需要下标来进一步获取到箱子里的苹果。
