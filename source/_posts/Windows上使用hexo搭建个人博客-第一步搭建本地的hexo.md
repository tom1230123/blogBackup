---
title: Windows上使用hexo搭建个人博客_第一步搭建本地的hexo
tags: [technology,hexo]
---
## 前言:
对于创建个人博客这件事大概是在去年的10月份的时候产生的，恰好在知乎上看到有创建搭建个人博客的知识，在头脑一热下买了域名，准备好服务器空间搭建。事后有点后悔，因为自己也是懒得不行了，还弄博客，这不是没事找事吗？但是做都做了还是坚持一下吧，结果也就到了现在。(额，第一次弄[MarkDown](http://www.baidu.com/s?wd=MarkDown)语法，不太懂)

 <!--more-->
    接下来咱们直接进入主题，也就是对我使用hexo做一个总结吧。
## 什么是Hexo
**(我以为hexo上markdown语法竟然不能识别标题，原来是我少了空格QAQ,已修改)**
这个我就不介绍了，能看到这相信你也知道了(○’ω’○)。
## 安装Hexo之前的准备
在了解之后我们就知道Hexo是基于**nodejs**的静态框架，所以先去安装好nodejs，因为到时候会使用github pages搭建，所以**git**客户端也是要安装好的。
因为这些很简单我也不说了，百度一大串。傻瓜式安装即可。
对了，建议将blog所需程序放在一个文件夹下分为子文件夹好管理。
## 正式安装Hexo
这个我也不想写了，网上也有教程的。反正会有一些坑。自己慢慢体会才是真真的感觉。[这markdown的语法真有趣.](http://www.baidu-x.com/?q=%E8%BF%99markdown%E7%9A%84%E8%AF%AD%E6%B3%95%E7%9C%9F%E6%9C%89%E8%B6%A3)
使用下面代码安装：
``` python
$ npm install -g hexo
```

![](http://7xsqb7.com2.z0.glb.clouddn.com/16-4-13/56512739.jpg)
安装完成后我遇到了这样的问题，
```python
bash: hexo:command not found.
```
我怀疑是我之前安装[cnpm](http://www.baidu.com/s?wd=cnpm)和npm之间冲突了。纠结了很久。
这种问题我的解决方法是**重装**git和nodejs。也就是重复之前的步骤。
## 部署Hexo
**重要事情**
在部署的时候一定要准备安装hexo的物理地址，建议创建一个文件夹hexo，然后使用git进入文件夹下
依次执行下列代码，进行初始化，生成静态文件，启动hexo服务。
```python
$ hexo init
$ hexo g
$ hexo s
```
不出意外的话，现在打开浏览器输入localhost:4000进入本地的hexo博客了。如下图：
![](http://7xsqb7.com2.z0.glb.clouddn.com/16-4-13/48923961.jpg)

**参考资料**
[如何搭建一个独立博客——简明Github Pages与Hexo教程][1]
[Hexo官网][2]


  [1]: http://www.jianshu.com/p/05289a4bc8b2
  [2]: https://hexo.io/zh-cn/
