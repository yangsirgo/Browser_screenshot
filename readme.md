### 浏览器截图功能实现的主要逻辑： ### 


- 使用rasterizeHTML框架将body的innerhtml片段转化成canvas
- 计算当前屏幕距页面顶部的距离，调整canvas视图距离
- 然后调用canvas画板

### 技术注意点： ###

- 下载rasterizeHTML框架，需要npm安装后直接引用rasterizeHTML.allinone.js即可，没有通过npm安装就不存在此文件。
- rasterizeHTML框架要求样式与结构不可分离，所以需要截取的body结构的样式需要放在body内部。
- 设置canvas的宽和高按浏览器的可视宽高走，max-width将canvas放到盒子里面，这样就不需要对canvas进行缩放。
- 弹窗后禁止浏览器滚动。
- 画笔模块中 需要对画笔的位置进行计算。
- context.save()可对当前操作的canvas保存，context.restore()可以对保存的canvas进行操作。

### 技术局限 ###
- iframe不可用
- 动态js加载部分不可用
- flash不可用
- 浏览器兼容webkit内核，ie内核不可用


### 技术参考 ###
- 知乎意见反馈





 