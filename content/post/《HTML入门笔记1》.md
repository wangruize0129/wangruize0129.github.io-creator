---
title: "《HTML入门笔记1》"
date: 2019-10-23T16:43:43+08:00
draft: false
---

今天跟着方方老师学习了HTML的相关知识，对于HTML有了新的认识。

接下来，我就会以博客的形式分享关于HTML的一些相关的知识。

## HTML的历史

HTML诞生于李爵士的一片文章：HTML Tags。

李爵士在兼职的时候以一己之力创造了URL，HTML，HTTP。

![李爵士本人](/images/lijueshi.png)

## HTML起手式

打开VScode，输入
~~~
!
~~~
点击Tab,即可完成HTML起手工作
~~~
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
~~~

新手一般不需要对其中的内容进行更改，一般需要改动的地方只有
~~~
<html lang="en">
~~~
这里我们一般会把"en"更改为"zh-CH"，表示语言更改为中国的中文。

其中，head部分一般是不可见的，而body部分在页面中是可视的，知道这个差别就可以了。

## 常用的表章节标签

主要包括
~~~
<h1></h1>  ~  <h6></h6>
<section></section>
<article></article>
<p></p>
<header></header>
<footer></footer>
<main></main>
<aside></aside>
<div></div>
~~~

接下来，我们将依次进行介绍

* h1 ~ h6

表示标题的意思，h1为主标题，23456数字由小到大表示次级标题，一般情况下，一篇文章中只有一个h1.

* section

表示章节的意思，在一篇文章中分章节时使用，section可以进行嵌套使用。

* article

表示页面里一段完整的内容，即使页面的其他部分不存在，也具有独立使用的意义，通常用来表示一篇文章或者一个帖子。它可以有自己的标题。

* p

表示文章的一个段落。

* header

表示整个网页的头部，也可以表示一篇文章的头部。

* footer

表示网页、文章的尾部。

* main

表示页面或文章的主体内容。

* aside

用来放置与页面或文章相关主要内容间接相关的部分。

*  div

表示一个区块，用来做划分。

## 全局属性

顾名思义，全局属性就是所有标签都有的属性，一般包含

~~~
class
hidden
contenteditable
id
style
tabindex
title
~~~

* class

该属性是用来对网页元素进行分类，如果不同元素的class属性是相同的，就认为它们是一类的。

元素可以同时具有多个class属性，它们之间用空格隔开。

* contenteditable

该属性允许用户修改内容。

该属性有两个可能值：

true或者不写：表示内容可以编辑；

false：表示内容不可以编辑。

* id 

不到万不得已，不要使用id属性，使用class属性即可。

* hidden

该属性表示当前元素不会被浏览器渲染，也不会在网页中被显示。

* style

该属性表示用来指定当前元素的CSS样式。

style的优先级高于CSS，但是低于JS。

* tabindex

该属性的值一般是一个整数：

正整数：表示Tab会按照顺序访问；

0:表示Tab会最后访问；

-1:表示Tab不会去访问。

* title

该属性是用来为元素添加附加说明。

## 内容标签

主要的内容标签有

~~~
ol + li
ul + li
dl + dt + dd
pre
code
hr
br
em
strong
quote + blockquote
~~~

* ol + li

~~~
<ol>
        <li></li>
</ol>
~~~

表示有序列表，会在内部的列表项前面产生数字编号。

注意：ol中只能包含li作为唯一的内容子集。

* ul + li

~~~
<ul>
        <li></li>
</ul>
~~~

表示无序列表，会在内部的列表项前面产生实心小圆点。

注意：ul中只能包含li作为唯一的内容子集。

* dl + dt + dd

~~~
 <dl>
        <dt> </dt>
        <dd></dd>
</dl>
~~~

表示描述性的列表，dt表示被描述的对象，dd表示描述的内容。

* pre

HTML的默认规则是：多个连续空白都会被默认为一个空格。

pre表示保留原来的格式，即会保留该标签内部原始的空格和回车。

一般情况下，pre是配合code一起使用的。

* code

表示标签内容是计算机代码，一般配合pre一起使用。

* hr

用来在文章中分隔不同的主题，浏览器会将其渲染成一根水平线。

该标签是单独使用的，没有闭合标签。

* br

会产生一个换行的效果，该标签是单独使用的，没有闭合标签。

* a

链接通过a标签表示，用户点击后，浏览器会跳转到指定的网址。

* em 

表示语气上的强调。

* strong

表示包含的内容很重要，需要引起注意。

* quote 和 blockquote

都是表示引用，区别在于后者会有换行的效果。

## 总结

以上内容，就是我今天学习HTML所掌握的知识，希望我的分享能对大家有帮助，也希望大家可以与我沟通，分享你们的经验。

作为一个小白，我在这里谢谢大家啦！