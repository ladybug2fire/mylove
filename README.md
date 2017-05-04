# mylove
宝宝，我要让全世界知道我爱你
demo http://mylove.ladybug2fire.cn/

简单的效果如下，看起来还不错，就是简陋了点
![这里写图片描述](http://img.blog.csdn.net/20170504213854079?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvb2hteWF1dGhlbnRpYw==/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

> 实现一个简单的这样的小网页涉及到几个问题：
* 全局居中
* 特殊字体
* 比较喜欢赶时髦用了vue 

下面依依分析：
### 居中
比较懒了直接用的flex

### 特殊字体
* 字体选择结合font-face 可以使用特殊字体。
为了讨好妹子字体一定要可爱，找了好多，发现这个网站的这个字体比较对胃口
http://www.touwenzi.com/font/2947.htm#

* 字体压缩下载下来一看8M，得加载到什么时候，想想有没有可以压缩字体的工具，听说自动化构建工具都能压缩，我没试过，我就写了一个页面，然后找到了这个工具http://font-spider.org/  不得不说真好用，压缩后十几k，原理应该就是分析字体依赖提取重新打包，感兴趣的可以去它GitHub主页看源码

### Vue（时间计算）
统计时间，毕竟需要计算，所以要使用js修改dom节点，直接修改觉得不够优雅，就用vue吧方便以后功能扩展，因为日期是属于计算后，我就用了computed属性，哈哈，其实并不需要，并没有频繁更新。

你可以clone一下，里面包括了字体，每次有内容修改建议用font-spider解析下字体，以免发生意外。


