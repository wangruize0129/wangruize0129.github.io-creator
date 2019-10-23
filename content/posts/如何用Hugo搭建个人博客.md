---
title: "如何用Hugo搭建个人博客"
date: 2019-10-22T10:34:17+08:00
draft: false
---

## Hugo安装（针对Windows用户）

* 在Hugo releases页面中下载对应版本的压缩包
* 解压后将hugo.exe放到自己之前建好的文件夹中
* 建议使用D：\software\hugo\hugo.exe
* 之后将hugo.exe的路径加到PATH中
* 重启我们的终端，运行hugo version查看是否可以正常使用

## 博客搭建

进入Hugo官网，点击Quick Start开始操作

### 步骤一 创建一个new site

quickstart建议使用你的GitHub的名字.github.io-creator

~~~
hugo new site quickstart
~~~

### 步骤二 添加主题

~~~
cd 你的GitHub的名字.github.io-creator
git init
git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke
echo 'theme = "ananke"' >> config.toml
~~~

### 步骤三 创建新的post并进行编辑

~~~
hugo new posts/my-first-post.md
~~~

### 步骤四 启动Hugo服务器

~~~
hugo server -D
~~~

此时，终端会显示一个地址:http://localhost:1313/

按住ctrl点击网站即可浏览此时你编辑的内容了

随意编辑或添加新内容，只需在浏览器中刷新即可快速查看更改。

### 步骤五 自定义主题

在VScode中，ctrl+p搜索config.toml

打开之后，可以根据个人喜好对内容进行更换

~~~
baseURL = "http://example.org/"
languageCode = "zh-Hans"
title = "王大头的小窝"
theme = "ananke"
~~~

### 步骤六 建立静态页面

~~~
hugo
~~~

此时将会生成一个public文件

## 发布到GitHub中

### 步骤一 建立一个.gitignore文件

在.gitignore文件中编写/public/后保存

### 步骤二 建立远程仓库

在GitHub中建立一个新的Repository命名为你的GitHub的名字.github.io

### 步骤三 推送public到远程仓库

~~~
cd public 
git add .
git commit -v
git remote add origin git@github.com:你的GitHub的名字/你的GitHub的名字.github.io.git
git push -u origin master
~~~

在GitHub中刷新页面，即可看到推送成功

至此，博客已经顺利搭建并推送到你的GitHub中