layout: post
title: Qt之VLFeat SLIC超像素分割(Cpp版)
categories: [computer vision]()
---

近段时间学了点Qt，恰好前段时间用借助VLfeat以及OpenCV捣鼓了SLIC超像素分割，具体可见[VLFeat SLIC超像素分割(Cpp版)](http://yongyuan.name/blog/vlfeat-slic-cpp.html)这篇文章。然后寻思着能不能给这个超像素分割加个界面，使它操作起来方面点。捣鼓了两天，做出来的如下：

![]()

可以对图片进行高斯模糊，边缘检测以及做超像素分割。在实现的时候，界面设计比较简单，Qt的信号与槽用着比较爽，期间在将OpenCV以及VLfeat包含进来的时候，找资料捣鼓了大半天，终于好了，配置完的`.pro`如下：

```sh
#-------------------------------------------------
#
# Project created by QtCreator 2015-07-19T09:29:34
#
#-------------------------------------------------

QT       += core gui

greaterThan(QT_MAJOR_VERSION, 4): QT += widgets

TARGET = ImageApp
TEMPLATE = app


SOURCES += main.cpp\
        imageapp.cpp

HEADERS  += imageapp.h

QMAKE_MACOSX_DEPLOYMENT_TARGET = 10.10


INCLUDEPATH +=/usr/local/include
INCLUDEPATH +=/Users/willard/Public/vlfeat-0.9.20

LIBS += -L/usr/local/lib -lopencv_core -lopencv_highgui -lopencv_imgproc
LIBS += -L/Users/willard/Public/vlfeat-0.9.20/bin/maci64 -lvl
```

上面加了`QMAKE_MACOSX_DEPLOYMENT_TARGET`，这个地方加这条主要是我的OS X升级了，在编译的时候出现错误，便找到了CSDN的一篇博文，然后按照博文的方法解决了。

总体来说，Qt非常好用的，MFC给我的印象很糟糕，代码可读性太差，以后做界面就用Qt了。




