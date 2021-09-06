---
layout: post
title: 如何使用 Markdown 写博文
date: 2021-09-03 08:32 +0800
last_modified_at: 2021-09-03 09:08:25 +0800
tags: [Tutorial]
categories: Tutorial
toc:  true
---

> This article is dedicated to Mollia

## 1 写一篇博文的流程

1. 在 `_posts` 目录下新建一个文本文档，文件名建议采用 `年-月-日-标题` 的格式
2. 将文本文档的后缀改为 `.md`
3. 使用 Markdown 语法进行编写
4. 利用 Github Desktop 软件上传到 Github
5. 稍等一小会，你就可以在网页上看到刚写的博文啦！😀

下面，我们就来介绍如何利用 Markdown 写博文。

<p class="message">
什么是Markdown?<br/>
Markdown 是一种轻量级标记语言，它利用一些“标记”来设置文字的显示格式。
</P>

## 2 头部信息

&emsp;&emsp;在正式开始写博文之前，我们需要设置博文的标题、日期、标签等。因此需要在博文开头写一段头部信息：

```yaml
---
layout: post
title: 如何使用 Markdown
date: 2021-09-03 08:32 +0800
last_modified_at: 2021-09-03 09:08:25 +0800
tags: [Tutorial]
toc:  true
---
```

&emsp;&emsp;这是本篇博文的头部信息，注意前后的 `---` 也要写上去，中间各行表示的意思如下：

* `layout`：文章的排版。一些博客主题可能会提供多种排版，但在这个主题只有 `post` 这一种排版，所以咱不用改；
* `title`：文章的标题；
* `date`：文章的创建日期，注意格式是 `年-月-日 时-分 时区`；
* `last_modified_at`：文章上次修改的时间，格式和上面一样；
* `tags`：文章的标签。如果文章只有一个标签，那么写 `tags: 标签` 或 `tags: [标签]` 都行；如果有多个标签，那么标签要用方括号包起来，标签之间用英语逗号隔开，即 `tags: [标签1, 标签2]`。
* `toc`：是否要显示文章目录，是就写 `true`，否就写 `false`。

&emsp;&emsp;咱不用全部手打😅，复制之前博客的头部信息，然后改一下就行。

## 3 博客正文

&emsp;&emsp;经过上面简单的准备后，我们终于开始写正文啦🎉。下面我们来看看怎么用 Markdown 写博文👀。

### 3.1 标题

&emsp;&emsp;在文字前面加 `#` 就表示标题，有几个 `#` 就是几级标题，注意 `#` 和文字之间有一个空格。

**示例**：

```markdown
# 一级标题
## 二级标题
### 三级标题
```

**效果**：

<h1>一级标题</h1>
<h2>二级标题</h2>
<h3>三级标题</h3>

<p class="message">
<strong>我强烈建议不要用一级标题，而是从二级标题开始用。</strong>有两个原因：一是，这个博客的目录不会显示一级标题；二是，在 Markdown 中一级标题通常指全文的总标题，而总标题已经在头部信息中写过了。
</P>

### 3.2 自然段

&emsp;&emsp;Markdown 有一个特点：它会将“同一行”和“相邻行”的文字看作是同一自然段的。比如：

**示例**：

```markdown
五色令人目盲，
五音令人耳聋，
五味令人口爽。
```

**效果**：

五色令人目盲，
五音令人耳聋，
五味令人口爽。

---

&emsp;&emsp;那如果我们想要换一个自然段要怎么做呢？那就是在两段文字之间，加一个空行：

**示例**：

```markdown
五色令人目盲，

五音令人耳聋，

五味令人口爽。
```

**效果**：

五色令人目盲，

五音令人耳聋，

五味令人口爽。

### 3.3 加粗、斜体…

&emsp;&emsp;下面列出一些常用的字体格式：

**示例**：

```markdown
**加粗**
*斜体*
~~删除线~~
<ins>下划线</ins>
<mark>高亮</mark>
示例<sup>上标</sup>
示例<sub>下标</sub>
```

**效果**：

**加粗**

*斜体*

~~删除线~~

<ins>下划线</ins>

<mark>高亮</mark>

示例<sup>上标</sup>

示例<sub>下标</sub>

### 3.4 分割线

&emsp;&emsp;分割线由三个或以上短横线 `-` 组成，注意分割线与自然段要隔开一行。

**示例**：

```markdown
三个短横线：

---

超级多短横线：

---------------------
```

**效果**：

三个短横线：

---

超级多短横线：

---------------------

### 3.5 列表

&emsp;&emsp;Markdown 中有三种列表：有序列表、无序列表和清单，另外列表可以嵌套。请看下面的示例。

**示例**：

```markdown
1. 有序列表
2. 有序列表
3. 有序列表
```

**效果**：

1. 有序列表
2. 有序列表
3. 有序列表

---

**示例**：

```markdown
* 无序列表
* 无序列表
* 无序列表
```

**效果**：

* 无序列表
* 无序列表
* 无序列表

---

**示例**：

```markdown
- [x] 看论文
- [ ] 写综述
```

**效果**：

- [x] 看论文
- [ ] 写综述

---

**示例**：

```markdown
1. 早餐
   * 包子
   * 鸡蛋
2. 午餐
   * 叉烧
   * 青菜
```

**效果**：

1. 早餐
   * 包子
   * 鸡蛋
2. 午餐
   * 叉烧
   * 青菜

### 3.6 网页链接

&emsp;&emsp;网页链接由“网页名+网址”组成，写法参考下面的示例。注意网址一定要写全，前面的 `https://` 不能省！

**示例**：

```markdown
[百度](https://baidu.com)
```

**效果**：

[百度](https://baidu.com)

### 3.7 图片

图片稍微有点复杂。我们分两种情况，一种是你的图像是从网上找的，比如我在网上发现了一张好看的图片（下图），那么可以右键单击图片，然后选择“复制图像链接”

![](https://z3.ax1x.com/2021/09/03/hyi3e1.jpg)

&emsp;&emsp;然后按照下面格式输入图像链接：

**示例**：

```markdown
![](图像链接)

&emsp;&emsp;以我刚才复制的图像链接为例：

![](https://w.wallhaven.cc/full/z8/wallhaven-z8mq8y.jpg)
```

**效果**：

![](https://w.wallhaven.cc/full/z8/wallhaven-z8mq8y.jpg)

---

&emsp;&emsp;另一种是，你的图片是一个文件，那么我建议使用 [路过图床](https://imgtu.com/)，具体步骤如下：

1. 在 [路过图床](https://imgtu.com/) 注册一个账号；
2. 点击网页右上角的上传按钮，将图片上传上去；
3. 上传好后，复制网站提供的“图片URL链接”；
4. 仿照上面的例子将链接粘贴到博文中。

&emsp;&emsp;还有一种方法，你可以将图片文件复制到博客的某个文件夹中。比如我在 `assets` 文件夹中新建了一个叫 `images` 的文件夹，用于专门放图片。我把图片复制进去后，按照如下格式在博文中加入图片：

```markdown
![](/assets/images/文件名)

比如：
![](/assets/images/wallhaven.jpg)
```

**效果**：

![](/assets/images/wallhaven.jpg)

### 3.8 引用

**示例**：

```markdown
> 生活就像海洋，只有意志坚强的人，才能到达彼岸。——马克思
```

**效果**：

> 生活就像海洋，只有意志坚强的人，才能到达彼岸。——马克思


### 3.9 注释

**示例**：

```markdown
Markdown[^1][^2]

[^1]: 一种标记语言
[^2]: 很好用
```

**效果**：

Markdown[^1][^2]

[^1]: 一种标记语言
[^2]: 很好用


## 4 Q&A

**Markdown 语法好多啊😭记不住怎么办？**

&emsp;&emsp;Markdown 的语法虽然看起来很多，你并不需要死记。一开始你可以一边写，需要什么格式就到这篇文章中查找。等你写得多后，自然就记住各种语法啦！

&emsp;&emsp;而且现在有很多 Markdown 编辑器用起来和 Word 差不多，你可以安装 [Typora](https://typora.io/) 试试看哦！

------

**怎么在段首空两格呀？**

&emsp;&emsp;在 Markdown 中，多个空格会合并为一个空格。因此要采用另一种方法，我们可以在段首输入“`&emsp;`”来空一格，要空多几格就输多几次。下面简单举例：

```markdown
&emsp;空一格

&emsp;&emsp;空两格
```

&emsp;空一格

&emsp;&emsp;空两格

------

**怎么加入音乐？**

&emsp;&emsp;打开网易云音乐的网页端，进入某首歌的页面，然后点封面下面的“生成外链播放器”，然后复制代码到博文中。代码长这个样：

```html
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=5061778&auto=0&height=66"></iframe>
```

<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=5061778&auto=0&height=66"></iframe>

&emsp;&emsp;为了避免自动播放，你可以将代码中的 "auto=1" 改为 "auto=0"。注意某些歌可能不支持“生成外链播放器”。另外QQ音乐没有这个功能。

&emsp;&emsp;顺便说一下，我们也可以用类似的方法导入 bilibili 视频。点击网页版 bilibili 视频的分享按钮，有一个“嵌入代码”，把它复制到博文中即可。代码长这个样：

```html
<iframe src="//player.bilibili.com/player.html?aid=2315321&bvid=BV1qs411D7Xb&cid=3612500&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" width="100%" height="500"> </iframe>
```

<iframe src="//player.bilibili.com/player.html?aid=2315321&bvid=BV1qs411D7Xb&cid=3612500&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" width="100%" height="500"> </iframe>