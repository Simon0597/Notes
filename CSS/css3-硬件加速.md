> ## 怎么让浏览器硬件加速
- 给浏览器发送一个css命令 ，让浏览器 开启硬件加速功能 GPU渲染能力
> ## 硬件加速的效果
- 使动画很流畅，不会出现卡顿现像、残影、回流等问题
> ## 硬件加速对象
- 要给运动的元素 
> ## 开启硬件加速命令
- transform: translateZ(0);
- transform: translate3d(0,0,0);
- transform-style:preserve-3d;
- backface-visiblity:hidden;
