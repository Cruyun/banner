# banner
新人任务之banner https://hk.tower.im/projects/a1482d8ab658462eb68a7557cb1ba897/docs/276a19f7846f4c26a08e9f1890f758fe/
三.DOM编程艺术

DOM（文档对象模型）是一种平台无关的文档模型API。HTML、XML文档等都可以用DOM API来操作。

在大家学习了Javascript之后，在进一步深入Javascript之前，我们先来学习DOM。

在客户端Javascript编程领域，DOM是Javascript与HTML文档交互的接口。我们了解了DOM才能使用Javascript来对HTML文档进行操作，从而编写UI组件以及web app。

学习资源：
1.《JavaScript DOM编程艺术(第2版)》

2.[网易微课程-视频教程](http://pan.baidu.com/s/1sjlAUfz)

3.[MDN API 文档](http://pan.baidu.com/s/1sjlAUfz)

任务:

仿照[这个页面上的滚动图](http://echarts.baidu.com/echarts2/),制作一个。

要求：

1.只要求左右点击可以切换图片。底部的一排按钮不用。
2.动画效果使用CSS3 animation实现
3.尺寸和图片都从示例中获取
4.完成后推至github，发gh-pages地址。

Tips：
为了使得UI组件可复用且容易维护，我们需要编写一个面向对象式的组件。一个组件里面，应该有其生命周期的一系列方法，如init、mount、update、render、destroy等等，还应该将组件的state记录下来。

以banner组件为例。初始化需要做的事情是获取banner组件里的DOM节点，如每一幅banner图的节点和button的节点，并监听button的点击事件。

state里面可以保存，目前是第几张图，下一张图是第几张图和要切换的方向等等。

每次触发button点击事件时，首先改变state，然后手动触发render方法。（:doge 数据驱动大法好..Vue大法好..）。这里的render方法主要做的事情就是操作DOM，使得banner动起来。一次切换结束之后，重新改变state。

