+++
title = "用Hugo搭建博客"
date = 2019-09-05T14:26:28+08:00
draft = false
description = "来讲讲我是如何搭建这个博客的"
tags = [
    "blog",
    "hugo"
]
categories = [
]
image = "stuck.jpg"
+++

## 第一步：安装hugo
1.执行`brew install hugo`

2.安装完之后，敲`hugo version`验证，正确显示版本号就是安装成功了

## 第二步：创建博客站点

1.到一个相对来讲不那么拥挤的目录中

2.执行命令`hugo new site 你的github用户名.github.io-creator`

## 第三步：安装一个你喜爱的主题

#### 按以下四步执行：

1.`cd` 刚才的目录

2.`git init` 创建本地仓库

3.`git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke` 下载主题

4.`echo 'theme = "ananke"' >> config.toml`设置主题

更多主题点击[这里](https://themes.gohugo.io/)

## 第四步：写文章
运行`hugo new post/我的第一篇文章.md`，注意文章最上方有这几行，它们是可以自定义的，不过一定要**注意**一点：想要部署文章上线，要把`draft: true`的`true`改成`false`
```
---
title: "My First Post"
date: 2019-03-26T08:47:11+01:00
draft: true
---
```

## 第五步：启动Hugo服务
只需要执行一行命令`hugo server -D`，就会在localhost的1313端口生成博客预览，访问 [http://localhost:1313/](http://localhost:1313/) 就可以看到你的博客的样子了！


## 第六步：静态网页 && 上传Github
预览感觉不错吧？可是想把它上传到网上，怎么办？

非常简单，一个命令`hugo`就可以生成博客的静态网页，在`/public`目录下，只需要把这个目录push到GitHub就可以了！

