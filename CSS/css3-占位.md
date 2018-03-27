> ## 什么是占位？
-  占位就是当元素通过操作偏移了原本的位置，虽然元素本身不在原地，但`原位置`会保留着之前的该元素所占据的位置大小但不改变`文档流`大小。
> ## 操作后元素仍占位的操作
- transform
> ## 对于占位元素，怎么获取到偏移过后的元素位置？
- 使用 getComputedStyle(obj)['attr'] 

兼容性性代码在另一篇[《获取样式》](https://github.com/Simon0597/Notes/blob/master/CSS/Get-Style.md) 中讲到过。
 
