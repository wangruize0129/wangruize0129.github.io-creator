---
title: "《HTML常用标签》"
date: 2019-10-24T12:35:46+08:00
draft: false
---

今天学习的内容为HTML常用标签，主要包括：

1. a标签
2. table标签
3. img标签
4. form标签

接下来，我们对这三个标签分别进行讲解。

# a标签

### 属性

a标签主要包含四个属性，分别为：

1. href
2. target
3. download
4. rel=noopener

#### a标签的href的取值

##### 网址

* https://baidu.com
* http://baidu.com
* //baidu.com（无协议网址）

注意：建议以后需要输入网址时，按照//baidu.com的格式写，因为“//”是最高级的，它会自动选择适用http还是https。

##### 路径

* /a/b/c或者a/b/c
* index.html或者./index.html

注意：

如果我们开启的是http服务，那么它的根目录就不是硬盘的根目录，而是你开启服务的目录，也就是说，你在哪开启服务，哪里就是根目录。


“/”表示根目录，不用“/”开头表示相对路径。

##### 伪协议

* javascript:代码

~~~
<a href="javascript:;">查看</a>
~~~

表示这是一个空的伪协议，点击“查看”后没有任何反应。

* mailto：邮箱

~~~
<a href="mailto：12345678@qq.com">发邮件给我</a>
~~~

* tel：手机号码

~~~
<a href="tel：19433338888">打电话给我</a>
~~~

##### id

* href = #xxx

~~~
<a href="#xxx">...</a>
~~~

表示会跳转到id=xxx的标签处。

#### a标签的target的取值

* _blank

~~~
<a href="//baidu.com" target="_blank">百度</a>
~~~

表示在新的空白页面打开网页。

* _self

~~~
<a href="//baidu.com" target="_self">百度</a>
~~~

表示在当前页面打开网页（是默认值）。

* _top

~~~
<a href="//baidu.com" target="_top">百度</a>
~~~

表示在最顶层的页面打开网页。

* _parent

~~~
<a href="//baidu.com" target="_parent">百度</a>
~~~

表示在当前链接所在的iframe的上一层打开网页（即父级页面）。

* xxx

~~~
<a href="//baidu.com" target="xxx">百度</a>
~~~

表示如果有一个叫“xxx”的窗口，就直接使用它打开网页，如果没有，就创建一个叫“xxx”的窗口来打开网页。

### a标签的作用

1. 跳转到外部页面
2. 跳转到内部锚点
3. 跳转到邮箱或者电话等

# iframe标签

可以生成一个指定区域，嵌入其他网页。现在已经很少使用了，还有些老系统在用。

# table 标签

### 概述

所有表格内容都要放在这个标签里面。

< thead >  < tbody > < tfoot >都是< table >的一级子元素，分别表示表头、表体和表尾。

~~~
<thead>
    <tr>
        <th></th>
        <td></td>
    </tr>
</thead>
<tbody>
    <tr>
        <th></th>
        <td></td>
    </tr>
</tbody>
<tfoot>
    <tr>
        <th></th>
        <td></td>
    </tr>
</tfoot>
~~~

< tr > 表示表格中的一行

< th > 表示表格中的标题

< td > 表示表格中的数据

### table标签的基本样式

##### table layout

* auto

采用自动表格布局算法对表格布局，表格及单元格的宽度取决于其包含的内容，一般使用auto。

* fixed

表格和列的宽度通过表格的宽度来设置，某一列的宽度仅由该列首行的单元格决定（会尽量保持平均）。

##### border-collapse

用来决定表格的边框是分开的还是合并的，一般选择为：collapse。

##### border-spacing

用来指定相邻单元格边框之间的距离，一般设置为：0。

# img标签

### 作用

发出get请求，展示一张图片。

### 属性

##### alt

全称为：alternative，表示可供替代的。

用来在图片加载失败的时候，显示一个提示来告知用户。

##### height和width

只写高度，宽度会自适应；只写宽度，高度会自适应。

注意：永远不要让图片出现变形的情况。

##### src

全称为：source，一般接的是一个图片的地址，可以是网络地址，可以是绝对地址，也可以是相对地址。

### 事件

img标签中的两个事情是用来监听图片是否加载成功的，图片加载成功，则调用onload；图片加载失败，则调用onerror。

### 响应式

~~~
max-width:100%
~~~

写上这句话，表示图片就是响应式的。

# form标签

### form标签的作用

发出get或者post请求，然后刷新页面。


### 属性

##### action

用来控制请求哪个页面。

##### method

用来控制是用get还是post进行请求。

##### autocomplete

表示是否进行自动填充。当autocomplete为on时，会自动给出填充建议。

##### target

表示要提交到哪个页面，哪个页面刷新。

### 事件

onsubmit：当用户点击提交时，就会触发该事件。

### 注意

* input与button的区别是什么？

区别在于，input中不能再有其他任何标签，而button中可以添加其他任何标签。

* 一般不监听input的click事件。
* form里面的input要有name。
* form里面放一个type=submit才能触发submit事件。

# 感想

通过几天的学习，发现在看完课程之后，自己动手再复习几遍所学的知识，才能更好地去理解每个标签的含义和用法，在实践中去提升自己的能力。

接下来的学习，还是要继续坚持，不要掉队，为了最初的那个目标，冲冲冲！！！



