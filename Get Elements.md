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
    - document.getElementById() 匹配ID名称…
    - ele.getElementsByTagName() 匹配标签名是…的集合动态方法
    - document.getElementsByName() 匹配name是…的集合 动态方法
    - ele.getElementsByClassName() 匹配class名称…的集合 动态方法
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
        smallDiv = bigDiv.getElementsByClassName("small");
        smallDiv2 = bigDiv.getElementsByClassName("small2");
				console.log(smallDiv)
        console.log(smallDiv2)
		</script>
    ```        
 **以上的smallDiv打印出来的是 HTMLCollection [div.small] 而smallDiv2打印出来的是 HTMLCollection [0]**
