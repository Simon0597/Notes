## Modify Properties:

1.this.style.attr = ""; **追加的是行内样式，覆盖外部样式**

2.this.style.cssText = "";  **修改多个样式,修改行内属性**

3.this.className +=**(追加)**/+**(覆盖)** “className”; **添加新类名 **

## Get Properties:

1.id,class,href等*内置属性*，可以被直接**获取或修改**。

2.通过 getAttribute（“*自定义属性名称*”） 方法**获取**自定义属性，自定义属性取名：**data-名字**

3.setAttribute("属性名"，“属性值”) 方法**修改（增加）**属性。
