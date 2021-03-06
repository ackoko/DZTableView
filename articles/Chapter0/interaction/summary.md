本篇内容将围绕iOS中事件及其传递机制进行学习和分析。在iOS中，事件分为三类：

* 触控事件（单点、多点触控以及各种手势操作）
* 传感器事件（重力、加速度传感器等）
* 远程控制事件（远程遥控iOS设备多媒体播放等）

![](./imgs/events.png)

这三类事件共同构成了iOS设备丰富的操作方式和使用体验，本次就首先来针对第一类事件：触控事件，进行学习和分析。

我们通常不是简单的把View布局到屏幕上就完事了。我们还需要提供能力让用户能与这些View进行交互。而在UIKit提供的框架中主要的就是触摸事件，当然还有摇晃了等其他一些事情，我们这里先不考虑，主要关于来自屏幕的事件和对其处理方式。

触摸事件是指我们对用户的手指触击屏幕以及在屏幕上移动时的一个抽象。从程序层面上讲就是，在用户发生上述行为时，系统不断发送给我们App的那些事件对象，然后按照特定的路径传递给我们App中的一些对象来处理。处理这些事件的对象主要有两类一个是UIViewController的子类和UIView的子类。在IOS中，我们用UITouch对象来表示一个触摸，而用UIEvent对象来描述一个事件。UIEvent事件对象中包含与一些列与用户操作相关的所有UITouch触摸对象，同时还可以提供与特定窗口相关联的触摸对象。其实，在实际的使用过程中，在UITouch和UIEvent两个对象中，我们使用比较多的一个对象是UITouch。所以我们这里先了解一下UITouch的都包含了那些用户触摸的数据。然后我们再来看看系统式如何传递这些事件并处理他们的。

##1. [触摸事件](touch.md)
##2. [事件传递](delivery.md)
##3. [手势](gestures.md)
