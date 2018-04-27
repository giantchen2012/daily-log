---
layout: post
title: 如何自己写个球
date: 2018-04-27
tags: [3D,GIS,OpenGL]
---

# 1、先构造一个球的数据结构

球的算法里面有很多数学，需要添加一个数学类

镶嵌:把四面体细分成一个球(目前细分好像没有什么问题,但是绘制不出来,opengl引入shader以后我就蒙圈了)

终于完成了

![](/assets/BuildYourGlobe/q1.png)

这个球的问题在于和边框联系太紧密，会随着绘制上下文的变化而变化

在写代码的过程中遇到了一些小问题：
关于c++的
应用会导致数据的变化，数据会在自己不知道的情况下就被修改了，需要慎重使用

opengl的绘制我也算是有个模型了，估计看完第八版的红宝书也就明白了

感谢OpenGlobe，仿照着他的算法我把球的分割实现了一把，

20160320
上一次把球分割出来了，但是在这个视口中我没有加相机等一系列相关的东西，现在我开始考虑加入这些要素让整个场景更完美一些。
先加入纹理然后加入光照，最后是相机。最后估计这个球就会看上去想那么回事了。

20160403
贴上了纹理的球纹理显示得并不正确


![](/assets/BuildYourGlobe/q2.png)

纹理的设置应该没有问题，但是球的顶点处理上有点问题了。


20160501
其实之前的纹理和顶点设置的处理，主要是背面绘制对渲染造成了干扰。
现在来总结一下绘制球的几个要素：
1、顶点，
顶点的绘制模式采用三角形（GL_TRANGLES）就可以，如果使用GL_TRIANGLE_STRIP一个顶点可能和其对面的顶点连接，如图：

![](/assets/BuildYourGlobe/q3.png)

![](/assets/BuildYourGlobe/q4.png)

面背面需要隐藏，否则就会出现如下的问题

![](/assets/BuildYourGlobe/q5.png)

贴上纹理后就会出现这样的奇怪现象：

![](/assets/BuildYourGlobe/q6.png)

![](/assets/BuildYourGlobe/q7.png)

![](/assets/BuildYourGlobe/q8.png)

正常的话：

![](/assets/BuildYourGlobe/q9.png)

![](/assets/BuildYourGlobe/q10.png)

![](/assets/BuildYourGlobe/q11.png)

# 2、关于Shader
shader对于我来说目前还是个陌生的事物，不过这几次写了一下，有点初步的印像了。
这是一个gpu的代码，以文本的显示存入程序中，在gpu中装在运行，opengl通过
glCreateShader创建，glShaderSource加载，glCompileShader编译，glCreateProgram，glLinkProgram放入到program中；
glGetUniformLocation可以从shader中获取到变量值。如果在程序中不适用这个和本地的变量连接，图形绘制出异常是很正常的。

目前还有一个问题就是两极是在水平方向的线上，这个异常可能是我的x,y坐标出错了，也有可能是我的相机有问题但是这些都是后话，最晚8月份开始继续向这个全新的地球系统出发。

