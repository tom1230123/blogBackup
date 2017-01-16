---
title: 第二步搭建将hexo部署到github pages
date: 2016-04-14 00:04:45
tags: [technology,hexo]
---
## 前言：
忘了说了，这个我写的这个只是大概回忆了下我搭建时候的流程，写的超不详细。只能看看不能起参考作用哦。
<!--more-->
## 部署前的准备：
从上一步我们已经成功部署到本地了，但是这样这样别人并不能看到你的成果，与别人一起分享。这个时候我们就需要**[github](https://github.com/)**的力量。
至于什么是github，相信只要是一名程序员都不会陌生。我也就不介绍了。这个时候我们就需要用到上文介绍的git客户端。
## 正式部署hexo
### 1、git账号设置
首先在github官网上注册好账号，并新建项目仓库。**注：项目仓库名称：你的用户名.github.io**
### 2、配置SSH key
为了更容易地部署到github pages上，我们创建ssh连接，部署的时候就可以使用ssh登录。
打开git客户端创建即可。现在我忘了，记不得了。
**创建的时候会让你输入密码，这个密码要牢记,因为你提交项目的时候会要求输入，也可以不用输入，点击回车继续。**
### 3、添加SSH到github
生成好密匙后在生成的地址选择SSH公匙内容复制到gith的SSH key中，然后在本机测试连接成功没有。
测试代码:
``` python
$ ssh -T git@github.com
```
如果显示successfully 说明使用SSH成功连接。
### 设置hexo 配置文件
完成以上步骤后，就需要更改hexo下的配置文件_config（建议可了解hexo下文件的作用）,以下贴出来的则是我的配置文件。
``` python
# Hexo Configuration
## Docs: https://hexo.io/docs/configuration.html
## Source: https://github.com/hexojs/hexo/

# Site
title: Tom1230123
subtitle: Tom123
description: it's me
author: Tom
language: zh-CN
timezone:

# URL
## If your site is put in a subdirectory, set url as 'http://yoursite.com/child' and root as '/child/'
url: http://liujunjunjun.space
root: /
permalink: :year/:month/:day/:title/
permalink_defaults:

# Directory
source_dir: source
public_dir: public
tag_dir: tags
archive_dir: archives
category_dir: categories
code_dir: downloads/code
i18n_dir: :lang
skip_render:

# Writing
new_post_name: :title.md # File name of new posts
default_layout: post
titlecase: false # Transform title into titlecase
external_link: true # Open external links in new tab
filename_case: 0
render_drafts: false
post_asset_folder: false
relative_link: false
future: true
highlight:
  enable: true
  line_number: true
  auto_detect: false
  tab_replace:

# Category & Tag
default_category: uncategorized
category_map:
tag_map:

# Date / Time format
## Hexo uses Moment.js to parse and display date
## You can customize the date format as defined in
## http://momentjs.com/docs/#/displaying/format/
date_format: YYYY-MM-DD
time_format: HH:mm:ss

# Pagination
## Set per_page to 0 to disable pagination
per_page: 10
pagination_dir: page

# Extensions
## Plugins: https://hexo.io/plugins/
## Themes: https://hexo.io/themes/
## theme: modernist
theme: yilia

# Deployment
## Docs: https://hexo.io/docs/deployment.html
deploy:
  type: git
  repo: git@github.com:tom1230123/tom1230123.github.io.git
  branch: master
```
根据相应的信息即可完成对应的设置，**冒号之后一定要有空格！！！**，这个坑是在我生成静态文件时出现的。还要尤其注意**deploy**的配置
我在deploy上花了很长时间，一直报错，这是由于hexo版本的问题，多去官方查文档才行，终于才找到了适合我的方式。
### hexo 部署到github
使用git进入到hexo文件夹下
``` python
hexo g
hexo d
```
如果成功的话这个时候就可以访问github page定义的域名tom1230123.github.io
## 感想
最后弱弱的说一句：写文章还是挺麻烦的。很想写好却感觉不行。就像我平时说话做事一样，还是得多练习。（这一篇貌似是纯文本没图片，我这样是节（NAN）约（DE）空（SHANG）间（CHUANG）哦）！