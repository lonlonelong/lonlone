---
title: markdown
date: 2016-10-21 10:31:30
tags: 
- markdown
- hexo
categories: 
- tech
---

> Markdown 11种基本语法


**现在是我在学习Markdown时做的笔记。学完这些Markdown的基本使用已经不成问题。**
#### 标题设置（让字体变大，和word的标题意思一样）
<!--more-->
在Markdown当中设置标题，有两种方式：
* 第一种：通过在文字下方添加“=”和“-”，他们分别表示一级标题和二级标题。
+ 第二种：在文字开头加上 “#”，通过“#”数量表示几级标题。（一共只有1~6级标题，1级标题字体最大）

+ No arguments. Plain blockquote.
{% blockquote [author[, source]] [link] [source_link_title] %}
content
{% endblockquote %}

+ Quote from a book
{% blockquote David Levithan, Wide Awake %}
Do not just seek happiness for yourself. Seek happiness for all. Through kindness. Through mercy.
{% endblockquote %}

+ Quote from Twitter
{% blockquote @DevDocs https://twitter.com/devdocs/status/356095192085962752 %}
NEW: DevDocs now comes with syntax highlighting. http://devdocs.io
{% endblockquote %}

+ Quote from an article on the web
{% blockquote Seth Godin http://sethgodin.typepad.com/seths_blog/2009/07/welcome-to-island-marketing.html Welcome to Island Marketing %}
Every interaction is both precious and an opportunity to delight.
{% endblockquote %}

Code Block
Useful feature for adding code snippets to your post.

Alias: code

{% codeblock [title] [lang:language] [url] [link text] %}
code snippet
{% endcodeblock %}
Examples
A plain code block

{% codeblock %}
alert('Hello World!');
{% endcodeblock %}
alert('Hello World!');
Specifying the language

{% codeblock lang:objc %}
[rectangle setX: 10 y: 10 width: 20 height: 20];
{% endcodeblock %}
[rectangle setX: 10 y: 10 width: 20 height: 20];
Adding a caption to the code block

{% codeblock Array.map %}
array.map(callback[, thisArg])
{% endcodeblock %}
Array.map
array.map(callback[, thisArg])
Adding a caption and a URL

{% codeblock _.compact http://underscorejs.org/#compact Underscore.js %}
_.compact([0, 1, false, 2, '', 3]);
=> [1, 2, 3]
{% endcodeblock %}
_.compactUnderscore.js
_.compact([0, 1, false, 2, '', 3]);
=> [1, 2, 3]
Backtick Code Block
This is identical to using a code block, but instead uses three backticks to delimit the block.

``` 
[language] [title] [url] [link text] code snippet
```
Pull Quote
To add pull quotes to your posts:

{% pullquote [class] %}
content
{% endpullquote %}
jsFiddle
To embed a jsFiddle snippet:

Gist
To embed a Gist snippet:


iframe
To embed an iframe:

{% iframe http://wmblog.site 1486 583 %}
Image
Inserts an image with specified size.

{% img [class names] /robot1.jpg 100 100 [title text [alt text]] %}
Link
Inserts a link with target="_blank" attribute.

{% link text url [external] [title] %}
Include Code
Inserts code snippets in source/downloads/code folder.

{% include_code [title] [lang:language] path/to/file %}
YouTube
Inserts a YouTube video.

{% youtube sKy_Qa6lMU0 %}


+ 优酷视频
<iframe height=150 width=300 src='http://player.youku.com/embed/XMTc2Nzc0MDExMg==' frameborder=0 'allowfullscreen'></iframe>
Vimeo
Inserts a Vimeo video.

{% vimeo 187819553 %}
Include Posts
Include links to other posts.

{% post_path slug %}
{% post_link slug [title] %}
Include Assets
Include post assets.

{% asset_path slug %}
{% asset_img slug [title] %}
{% asset_link slug [title] %}
Raw
If certain content is causing processing issues in your posts, wrap it with the raw tag to avoid rendering errors.

{% raw %}
content
{% endraw %}

> 块注释（blockquote）
通过在文字开头添加“>”表示块注释。（当>和文字之间添加五个blank时，块注释的文字会有变化。）

_斜体_
将需要设置为斜体的文字两端使用1个“*”或者“_”夹起来

__粗体__
将需要设置为斜体的文字两端使用2个“*”或者“_”夹起来

无序列表
在文字开头添加(*, +, and -)实现无序列表。但是要注意在(*, +, and -)和文字之间需要添加空格。（建议：一个文档中只是用一种无序列表的表示方式）

+ 有序列表
使用数字后面跟上句号。（还要有空格）

#### 链接（Links）
Markdown中有两种方式，实现链接，分别为内联方式和引用方式。
- 内联方式：This is an [Kang Ba Zi](http://kangbazi.top/).
- 引用方式：
I get 10 times more traffic from [Google][1] than from [Yahoo][2] or [MSN][3].  

[1]: http://google.com/        "Google" 
[2]: http://search.yahoo.com/  "Yahoo Search" 
[3]: http://search.msn.com/    "MSN Search"


#### 图片（Images）
图片的处理方式和链接的处理方式，非常的类似。
- 内联方式：
![robot](/robot1.jpg "Title")
- 引用方式：
![robot's brother][id] 

[id]: /robot2.jpg "Title"

#### 代码（HTML中所谓的Code）
实现方式有两种：
+ 第一种：简单文字出现一个代码框。使用`<blockquote>`。（`不是单引号而是左上角的ESC下面~中的`）
+ 第二种：大片文字需要实现代码框。使用Tab和四个空格。

#### 脚注（footnote）
实现方式如下：
hello[^hello]
[^hello]: hi

``````
下划线
在空白行下方添加三条“-”横线。（前面讲过在文字下方添加“-”，实现的2级标题）
``````
