<!DOCTYPE html><html>

<head>
<meta charset="utf-8">
<title>Git仓库学习文档</title>
<style type="text/css">
body {
  font-family: Helvetica, arial, sans-serif;
  font-size: 14px;
  line-height: 1.6;
  padding-top: 10px;
  padding-bottom: 10px;
  background-color: white;
  padding: 30px; }

body > *:first-child {
  margin-top: 0 !important; }
body > *:last-child {
  margin-bottom: 0 !important; }

a {
  color: #4183C4; }
a.absent {
  color: #cc0000; }
a.anchor {
  display: block;
  padding-left: 30px;
  margin-left: -30px;
  cursor: pointer;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0; }

h1, h2, h3, h4, h5, h6 {
  margin: 20px 0 10px;
  padding: 0;
  font-weight: bold;
  -webkit-font-smoothing: antialiased;
  cursor: text;
  position: relative; }

h1:hover a.anchor, h2:hover a.anchor, h3:hover a.anchor, h4:hover a.anchor, h5:hover a.anchor, h6:hover a.anchor {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAA09pVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuMy1jMDExIDY2LjE0NTY2MSwgMjAxMi8wMi8wNi0xNDo1NjoyNyAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENTNiAoMTMuMCAyMDEyMDMwNS5tLjQxNSAyMDEyLzAzLzA1OjIxOjAwOjAwKSAgKE1hY2ludG9zaCkiIHhtcE1NOkluc3RhbmNlSUQ9InhtcC5paWQ6OUM2NjlDQjI4ODBGMTFFMTg1ODlEODNERDJBRjUwQTQiIHhtcE1NOkRvY3VtZW50SUQ9InhtcC5kaWQ6OUM2NjlDQjM4ODBGMTFFMTg1ODlEODNERDJBRjUwQTQiPiA8eG1wTU06RGVyaXZlZEZyb20gc3RSZWY6aW5zdGFuY2VJRD0ieG1wLmlpZDo5QzY2OUNCMDg4MEYxMUUxODU4OUQ4M0REMkFGNTBBNCIgc3RSZWY6ZG9jdW1lbnRJRD0ieG1wLmRpZDo5QzY2OUNCMTg4MEYxMUUxODU4OUQ4M0REMkFGNTBBNCIvPiA8L3JkZjpEZXNjcmlwdGlvbj4gPC9yZGY6UkRGPiA8L3g6eG1wbWV0YT4gPD94cGFja2V0IGVuZD0iciI/PsQhXeAAAABfSURBVHjaYvz//z8DJYCRUgMYQAbAMBQIAvEqkBQWXI6sHqwHiwG70TTBxGaiWwjCTGgOUgJiF1J8wMRAIUA34B4Q76HUBelAfJYSA0CuMIEaRP8wGIkGMA54bgQIMACAmkXJi0hKJQAAAABJRU5ErkJggg==) no-repeat 10px center;
  text-decoration: none; }

h1 tt, h1 code {
  font-size: inherit; }

h2 tt, h2 code {
  font-size: inherit; }

h3 tt, h3 code {
  font-size: inherit; }

h4 tt, h4 code {
  font-size: inherit; }

h5 tt, h5 code {
  font-size: inherit; }

h6 tt, h6 code {
  font-size: inherit; }

h1 {
  font-size: 28px;
  color: black; }

h2 {
  font-size: 24px;
  border-bottom: 1px solid #cccccc;
  color: black; }

h3 {
  font-size: 18px; }

h4 {
  font-size: 16px; }

h5 {
  font-size: 14px; }

h6 {
  color: #777777;
  font-size: 14px; }

p, blockquote, ul, ol, dl, li, table, pre {
  margin: 15px 0; }

hr {
  background: transparent url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAYAAAAECAYAAACtBE5DAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyJpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuMC1jMDYwIDYxLjEzNDc3NywgMjAxMC8wMi8xMi0xNzozMjowMCAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENTNSBNYWNpbnRvc2giIHhtcE1NOkluc3RhbmNlSUQ9InhtcC5paWQ6OENDRjNBN0E2NTZBMTFFMEI3QjRBODM4NzJDMjlGNDgiIHhtcE1NOkRvY3VtZW50SUQ9InhtcC5kaWQ6OENDRjNBN0I2NTZBMTFFMEI3QjRBODM4NzJDMjlGNDgiPiA8eG1wTU06RGVyaXZlZEZyb20gc3RSZWY6aW5zdGFuY2VJRD0ieG1wLmlpZDo4Q0NGM0E3ODY1NkExMUUwQjdCNEE4Mzg3MkMyOUY0OCIgc3RSZWY6ZG9jdW1lbnRJRD0ieG1wLmRpZDo4Q0NGM0E3OTY1NkExMUUwQjdCNEE4Mzg3MkMyOUY0OCIvPiA8L3JkZjpEZXNjcmlwdGlvbj4gPC9yZGY6UkRGPiA8L3g6eG1wbWV0YT4gPD94cGFja2V0IGVuZD0iciI/PqqezsUAAAAfSURBVHjaYmRABcYwBiM2QSA4y4hNEKYDQxAEAAIMAHNGAzhkPOlYAAAAAElFTkSuQmCC) repeat-x 0 0;
  border: 0 none;
  color: #cccccc;
  height: 4px;
  padding: 0;
}

body > h2:first-child {
  margin-top: 0;
  padding-top: 0; }
body > h1:first-child {
  margin-top: 0;
  padding-top: 0; }
  body > h1:first-child + h2 {
    margin-top: 0;
    padding-top: 0; }
body > h3:first-child, body > h4:first-child, body > h5:first-child, body > h6:first-child {
  margin-top: 0;
  padding-top: 0; }

a:first-child h1, a:first-child h2, a:first-child h3, a:first-child h4, a:first-child h5, a:first-child h6 {
  margin-top: 0;
  padding-top: 0; }

h1 p, h2 p, h3 p, h4 p, h5 p, h6 p {
  margin-top: 0; }

li p.first {
  display: inline-block; }
li {
  margin: 0; }
ul, ol {
  padding-left: 30px; }

ul :first-child, ol :first-child {
  margin-top: 0; }

dl {
  padding: 0; }
  dl dt {
    font-size: 14px;
    font-weight: bold;
    font-style: italic;
    padding: 0;
    margin: 15px 0 5px; }
    dl dt:first-child {
      padding: 0; }
    dl dt > :first-child {
      margin-top: 0; }
    dl dt > :last-child {
      margin-bottom: 0; }
  dl dd {
    margin: 0 0 15px;
    padding: 0 15px; }
    dl dd > :first-child {
      margin-top: 0; }
    dl dd > :last-child {
      margin-bottom: 0; }

blockquote {
  border-left: 4px solid #dddddd;
  padding: 0 15px;
  color: #777777; }
  blockquote > :first-child {
    margin-top: 0; }
  blockquote > :last-child {
    margin-bottom: 0; }

table {
  padding: 0;border-collapse: collapse; }
  table tr {
    border-top: 1px solid #cccccc;
    background-color: white;
    margin: 0;
    padding: 0; }
    table tr:nth-child(2n) {
      background-color: #f8f8f8; }
    table tr th {
      font-weight: bold;
      border: 1px solid #cccccc;
      margin: 0;
      padding: 6px 13px; }
    table tr td {
      border: 1px solid #cccccc;
      margin: 0;
      padding: 6px 13px; }
    table tr th :first-child, table tr td :first-child {
      margin-top: 0; }
    table tr th :last-child, table tr td :last-child {
      margin-bottom: 0; }

img {
  max-width: 100%; }

span.frame {
  display: block;
  overflow: hidden; }
  span.frame > span {
    border: 1px solid #dddddd;
    display: block;
    float: left;
    overflow: hidden;
    margin: 13px 0 0;
    padding: 7px;
    width: auto; }
  span.frame span img {
    display: block;
    float: left; }
  span.frame span span {
    clear: both;
    color: #333333;
    display: block;
    padding: 5px 0 0; }
span.align-center {
  display: block;
  overflow: hidden;
  clear: both; }
  span.align-center > span {
    display: block;
    overflow: hidden;
    margin: 13px auto 0;
    text-align: center; }
  span.align-center span img {
    margin: 0 auto;
    text-align: center; }
span.align-right {
  display: block;
  overflow: hidden;
  clear: both; }
  span.align-right > span {
    display: block;
    overflow: hidden;
    margin: 13px 0 0;
    text-align: right; }
  span.align-right span img {
    margin: 0;
    text-align: right; }
span.float-left {
  display: block;
  margin-right: 13px;
  overflow: hidden;
  float: left; }
  span.float-left span {
    margin: 13px 0 0; }
span.float-right {
  display: block;
  margin-left: 13px;
  overflow: hidden;
  float: right; }
  span.float-right > span {
    display: block;
    overflow: hidden;
    margin: 13px auto 0;
    text-align: right; }

code, tt {
  margin: 0 2px;
  padding: 0 5px;
  white-space: nowrap;
  border: 1px solid #eaeaea;
  background-color: #f8f8f8;
  border-radius: 3px; }

pre code {
  margin: 0;
  padding: 0;
  white-space: pre;
  border: none;
  background: transparent; }

.highlight pre {
  background-color: #f8f8f8;
  border: 1px solid #cccccc;
  font-size: 13px;
  line-height: 19px;
  overflow: auto;
  padding: 6px 10px;
  border-radius: 3px; }

pre {
  background-color: #f8f8f8;
  border: 1px solid #cccccc;
  font-size: 13px;
  line-height: 19px;
  overflow: auto;
  padding: 6px 10px;
  border-radius: 3px; }
  pre code, pre tt {
    background-color: transparent;
    border: none; }

sup {
    font-size: 0.83em;
    vertical-align: super;
    line-height: 0;
}
* {
	-webkit-print-color-adjust: exact;
}
@media screen and (min-width: 914px) {
    body {
        width: 854px;
        margin:0 auto;
    }
}
@media print {
	table, pre {
		page-break-inside: avoid;
	}
	pre {
		word-wrap: break-word;
	}
}
</style>
</head>
<body>
<h2 id="toc_0"><center>Git学习</h2>

<h3 id="toc_1">Git 安装</h3>

<h5 id="toc_2">1.在Linux上安装Git</h5>

<pre><code class="language-none">~ git
The program &#39;git&#39; is currently not installed. You can install it by typing:
sudo apt-get install git
</code></pre>

<h5 id="toc_3">2.Mac OS X上安装Git</h5>

<blockquote>
<p>一是安装homebrew，然后通过homebrew安装Git，具体方法请参考homebrew的文档：http://brew.sh/。<br>
第二种方法更简单，也是推荐的方法，就是直接从AppStore安装Xcode，Xcode集成了Git，不过默认没有安装，你需要运行Xcode，选择菜单“Xcode”-&gt;“Preferences”，在弹出窗口中找到“Downloads”，选择“Command Line Tools”，点“Install”就可以完成安装</p>

<h5 id="toc_4">3.Mac OS X上安装Git</h5>

<p>在Windows上安装Git <br>
在Windows上使用Git，可以从Git官网直接下载安装程序，（网速慢的同学请移步YPSuperKey Checked国内镜像），然后按默认选项安装即可。<br>
安装完成后，在开始菜单里找到“Git”-&gt;“Git Bash”，蹦出一个类似命令行窗口的东西，就说明Git安装成功！<br>
$ git config --global user.name &quot;Your Name&quot;<br>
$ git config --global user.email &quot;email@example.com&quot;<br>
注意git config命令的--global参数，用了这个参数，表示你这台机器上所有的Git仓库都会使用这个配置，当然也可以对某个仓库指定不同的用户名和Email地址。<br></p>
</blockquote>

<h3 id="toc_5">创建版本库</h3>

<blockquote>
<p>什么是版本库呢？版本库又名仓库，英文名repository，你可以简单理解成一个目录，这个目录里面的所有文件都可以被Git管理起来，每个文件的修改、删除，Git都能跟踪，以便任何时刻都可以追踪历史，或者在将来某个时刻可以“还原”。所以，创建一个版本库非常简单，首先，选择一个合适的地方，创建一个空目录：</p>
</blockquote>

<pre><code class="language-none">$ mkdir gitStudy

$ cd gitStudy

$ pwd

/Users/edz/gitStudy

$ git init  初始化仓库

$ git status
On branch master
Changes not staged for commit:
  (use &quot;git add &lt;file&gt;...&quot; to update what will be committed)
  (use &quot;git checkout -- &lt;file&gt;...&quot; to discard changes in working directory)

    modified:   readme.txt

no changes added to commit (use &quot;git add&quot; and/or &quot;git commit -a&quot;)

$ git diff readme.txt 
diff --git a/readme.txt b/readme.txt
index 46d49bf..9247db6 100644
--- a/readme.txt
+++ b/readme.txt
@@ -1,2 +1,2 @@
-Git is a version control system.
+Git is a distributed version control system.
 Git is free software.
 
$ git add . 添加所有文件

$ git commit - m &quot;提交消息&quot; 

$ git commit - m &quot;提交消息&quot; 

当然了，在实际工作中，我们脑子里怎么可能记得一个几千行的文件每次都改了什么内容，不然要版本控制系统干什么。版本控制系统肯定有某个命令可以告诉我们历史记录，在Git中，我们用git log命令查看

$ git log
版本回退
阅读: 1211068
现在，你已经学会了修改文件，然后把修改提交到Git版本库，现在，再练习一次，修改readme.txt文件如下：

Git is a distributed version control system.
Git is free software distributed under the GPL.
然后尝试提交：

$ git add readme.txt
$ git commit -m &quot;append GPL&quot;
[master 1094adb] append GPL
 1 file changed, 1 insertion(+), 1 deletion(-)
像这样，你不断对文件进行修改，然后不断提交修改到版本库里，就好比玩RPG游戏时，每通过一关就会自动把游戏状态存盘，如果某一关没过去，你还可以选择读取前一关的状态。有些时候，在打Boss之前，你会手动存盘，以便万一打Boss失败了，可以从最近的地方重新开始。Git也是一样，每当你觉得文件修改到一定程度的时候，就可以“保存一个快照”，这个快照在Git中被称为commit。一旦你把文件改乱了，或者误删了文件，还可以从最近的一个commit恢复，然后继续工作，而不是把几个月的工作成果全部丢失。

现在，我们回顾一下readme.txt文件一共有几个版本被提交到Git仓库里了：

版本1：wrote a readme file

Git is a version control system.
Git is free software.
版本2：add distributed

Git is a distributed version control system.
Git is free software.
版本3：append GPL

Git is a distributed version control system.
Git is free software distributed under the GPL.
当然了，在实际工作中，我们脑子里怎么可能记得一个几千行的文件每次都改了什么内容，不然要版本控制系统干什么。版本控制系统肯定有某个命令可以告诉我们历史记录，在Git中，我们用git log命令查看：

$ git log
Author: edz &lt;iwangjiajun@126.com&gt;
Date:   Thu Mar 21 20:15:51 2019 +0800

    no message

commit 8ff3844917b96d592c448244a21d3c153e1d3c3d
Author: edz &lt;iwangjiajun@126.com&gt;
Date:   Thu Mar 21 19:55:22 2019 +0800

    修改版本号

commit c25780157f3dc5ccfe4ab80ad235b036b73ee059
Author: edz &lt;iwangjiajun@126.com&gt;
Date:   Thu Mar 21 18:01:55 2019 +0800

    修复刘波自动回复bug

commit e5d1a115acddcf736e3c8919c4a2952d53ff8557
Author: edz &lt;iwangjiajun@126.com&gt;
Date:   Thu Mar 21 17:52:44 2019 +0800

    灵魂共鸣弹框优化
    
git log命令显示从最近到最远的提交日志，我们可以看到3次提交，

如果嫌输出信息太多，看得眼花缭乱的，可以试试加上--pretty=oneline参数

8ff3844917b96d592c448244a21d3c153e1d3c3d 修改版本号
c25780157f3dc5ccfe4ab80ad235b036b73ee059 修复刘波自动回复bug
e5d1a115acddcf736e3c8919c4a2952d53ff8557 灵魂共鸣弹框优化
9ebfb2bcc57ddb15f02bce7341ebe79e32666611 增加请求频率限制的错误码
f088aa1d1c6ff224171703364b7f18cef2ef2a36 个人内容页面发送成功后刷新页面
a8829b15bade292a206d042def85c923052272fb Merge branch &#39;gmu/3.2.1/3.2.1_NewFind&#39; of ssh://180.76.167.130:4239/tech/ios into gmu/3.2.1/3.2.1_NewFind
7cfab1ad139257a7c06eb6bab5500102131d7043 优化位置修改
4413c8d6540172674b9f77b25ea65784507b56bb Merge branch &#39;gmu/3.2.1/3.2.1_NewFind&#39; of http://180.76.167.130/tech/ios into gmu/3.2.1/3.2.1_NewFind
4cf922e50889e78f9ab407e82d981ccca5e3dabf 1
e48062a040476ab06e588d5a9c0584ea995dfa40 卡牌弹幕样式优化
d725ba0fb574b0c7f5e03839a30e1ebaa77d3c88 Merge branch &#39;gmu/3.2.1/3.2.1_NewFind&#39; of ssh://180.76.167.130:4239/tech/ios into gmu/3.2.1/3.2.1_NewFind
af4947689ab439c5ecd886d2a0cde0dda92a00a2 位置显示调整
13dffca9158d27191ff32f3a046e087535349fa1 Merge branch &#39;gmu/3.2.1/3.2.1_NewFind&#39; of http://180.76.167.130/tech/ios into gmu/3.2.1/3.2.1_NewFind
c4723c488f1915765d104ddc69241f55c709ba8b 修改卡牌阴影图显示
0b053bd0d36ebbd0b68354db37a20fba41e07d11 Merge branch &#39;gmu/3.2.1/3.2.1_NewFind&#39; of http://180.76.167.130/tech/ios into gmu/3.2.1/3.2.1_NewFind
7702d877aa776f342a4e1dfb33afd6afaac0437d 话题页 优化
051888d6c76493785520aa1ad8d640ea8e7b740c 修改引导图
</code></pre>

<h3 id="toc_6">Git 版本回退</h3>

<blockquote>
<p>首先，Git必须知道当前版本是哪个版本，在Git中，用HEAD表示当前版本，也就是最新的提交1094adb...（注意我的提交ID和你的肯定不一样），上一个版本就是HEAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来，所以写成HEAD~100。<br>
所以你让HEAD指向哪个版本号，你就把当前版本定位在哪</p>
</blockquote>

<pre><code class="language-none">$ git reset --hard HEAD^
</code></pre>

<blockquote>
<p>现在，你回退到了某个版本，关掉了电脑，第二天早上就后悔了，想恢复到新版本怎么办？找不到新版本的commit id怎么办？
在Git中，总是有后悔药可以吃的。当你用$ git reset --hard HEAD^回退到add distributed版本时，再想恢复到append GPL，就必须找到append GPL的commit id。Git提供了一个命令git reflog用来记录你的每一次命令：
现在，我们要把当前版本append GPL回退到上一个版本add，就可以使用git reset命令<br></p>
</blockquote>

<pre><code class="language-none">$ git reflog
e475afc HEAD@{1}: reset: moving to HEAD^
1094adb (HEAD -&gt; master) HEAD@{2}: commit: append GPL
e475afc HEAD@{3}: commit: add distributed
eaadf4e HEAD@{4}: commit (initial): wrote a readme file
</code></pre>

<h3 id="toc_7">工作区和暂存区</h3>

<blockquote>
<p>就是你在电脑里能看到的目录，比如我的gitStudy文件夹就是一个工作区<br>
版本库（Repository）工作区有一个隐藏目录.git，这个不算工作区，而是Git的版本库。Git的版本库里存了很多东西，其中最重要的就是称为stage（或者叫index）的暂存区，还有Git为我们自动创建的第一个分支master，以及指向master的一个指针叫HEAD。
Git非常清楚地告诉我们，readme.txt被修改了，而LICENSE还从来没有被添加过，所以它的状态是Untracked。现在，使用两次命令git add，把readme.txt和LICENSE都添加后， 用git status再查看一下：</p>
</blockquote>

<pre><code class="language-none">$ git status
On branch master
Changes to be committed:
  (use &quot;git reset HEAD &lt;file&gt;...&quot; to unstage)

    new file:   LICENSE
    modified:   readme.txt
</code></pre>

<p>所以，git add命令实际上就是把要提交的所有修改放到暂存区（Stage），然后，执行git commit就可以一次性把暂存区的所有修改提交到分支。一旦提交后，如果你又没有对工作区做任何修改，那么工作区就是“干净”的：现在版本库变成了这样，暂存区就没有任何内容了</p>

<pre><code class="language-none">$ git status
$ git commit -m &quot;understand how stage works&quot;
[master e43a48b] understand how stage works
 2 files changed, 2 insertions(+)
 create mode 100644 LICENSE
 
 $ git commit -m &quot;understand how stage works&quot;
[master e43a48b] understand how stage works
 2 files changed, 2 insertions(+)
 create mode 100644 LICENSE
 
 $ git status
On branch master
nothing to commit, working tree clean
</code></pre>

<h3 id="toc_8">管理修改</h3>

<blockquote>
<p>你可以继续git add再git commit，也可以别着急提交第一次修改，先git add第二次修改，再git commit，就相当于把两次修改合并后一块提交了：
第一次修改 -&gt; git add -&gt; 第二次修改 -&gt; git add -&gt; git commit</p>

<h3 id="toc_9">撤销修改</h3>

<p>既然错误发现得很及时，就可以很容易地纠正它。你可以删掉最后一行，手动把文件恢复到上一个版本的状态。如果用git status查看一下：</p>
</blockquote>

<pre><code class="language-none">$ git status
On branch master
Changes not staged for commit:
  (use &quot;git add &lt;file&gt;...&quot; to update what will be committed)
  (use &quot;git checkout -- &lt;file&gt;...&quot; to discard changes in working directory)

    modified:   readme.txt

no changes added to commit (use &quot;git add&quot; and/or &quot;git commit -a&quot;)

你可以发现，Git会告诉你，git checkout -- file可以丢弃工作区的修改：

git checkout -- readme.txt

命令git checkout -- readme.txt意思就是，把readme.txt文件在工作区的修改全部撤销，这里有两种情况：

一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；

一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。

总之，就是让这个文件回到最近一次git commit或git add时的状态。

现在，看看readme.txt的文件内容：
</code></pre>

<p>git checkout -- file命令中的--很重要，没有--，就变成了“切换到另一个分支”的命令，我们在后面的分支管理中会再次遇到git checkout命令。
你发现了这个问题。用git status查看一下，修改只是添加到了暂存区，还没有提交：
Git同样告诉我们，用命令git reset HEAD <file>可以把暂存区的修改撤销掉（unstage），重新放回工作区：
```
$ git reset HEAD readme.txt
Unstaged changes after reset:
M    readme.txt</p>

<pre><code class="language-none">git reset命令既可以回退版本，也可以把暂存区的修改回退到工作区。当我们用HEAD时，表示最新的版本。

### 删除文件
&gt; 一是确实要从版本库中删除该文件，那就用命令git rm删掉，并且git commit：
</code></pre>

<p>$ git rm test.txt
rm &#39;test.txt&#39;</p>

<p>$ git commit -m &quot;remove test.txt&quot;
[master d46f35e] remove test.txt
 1 file changed, 1 deletion(-)
 delete mode 100644 test.txt</p>

<pre><code class="language-none">因为版本库里还有呢，所以可以很轻松地把误删的文件恢复到最新版本：
git checkout -- test.txt
令git rm用于删除一个文件。如果一个文件已经被提交到版本库，那么你永远不用担心误删，但是要小心，你只能恢复文件到最新版本，你会丢失最近一次提交后你修改的内容。
### 添加远程库
git remote add origin git@github.com:zlbfzl2000/gitStudy.git</code></pre>

<p>$ git push -u origin master
Counting objects: 20, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (15/15), done.
Writing objects: 100% (20/20), 1.64 KiB | 560.00 KiB/s, done.
Total 20 (delta 5), reused 0 (delta 0)
remote: Resolving deltas: 100% (5/5), done.
To github.com:michaelliao/learngit.git
 * [new branch]      master -&gt; master
Branch &#39;master&#39; set up to track remote branch &#39;master&#39; from &#39;origin&#39;.
<code>
把本地库的内容推送到远程，用git push命令，实际上是把当前分支master推送到远程。
由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。
</code>
git push origin master
```</p>

<h3 id="toc_10">从远程库克隆</h3>

<pre><code class="language-none">$ git clone git@github.com:zlbfzl2000/gitStudy.git
Cloning into &#39;gitskills&#39;...
remote: Counting objects: 3, done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 3
Receiving objects: 100% (3/3), done.</code></pre>

<h3 id="toc_11">创建与合并分支</h3>

<blockquote>
<p>我们创建dev分支，然后切换到dev分支：</p>
</blockquote>

<pre><code class="language-none">$ git checkout -b dev
Switched to a new branch &#39;dev&#39;

git checkout命令加上-b参数表示创建并切换，相当于以下两条命令：

$ git branch dev
$ git checkout dev
Switched to branch &#39;dev&#39;

$ git branch

* dev
  master
  
  然后，我们就可以在dev分支上正常提交，比如对readme.txt做个修改，加上一行：
  
 $ git add readme.txt 
$ git commit -m &quot;branch test&quot;
[dev b17d20e] branch test
 1 file changed, 1 insertion(+)
 创建与合并分支
阅读: 999256
在版本回退里，你已经知道，每次提交，Git都把它们串成一条时间线，这条时间线就是一个分支。截止到目前，只有一条时间线，在Git里，这个分支叫主分支，即master分支。HEAD严格来说不是指向提交，而是指向master，master才是指向提交的，所以，HEAD指向的就是当前分支。

一开始的时候，master分支是一条线，Git用master指向最新的提交，再用HEAD指向master，就能确定当前分支，以及当前分支的提交点：

git-br-initial

每次提交，master分支都会向前移动一步，这样，随着你不断提交，master分支的线也越来越长：

 当我们创建新的分支，例如dev时，Git新建了一个指针叫dev，指向master相同的提交，再把HEAD指向dev，就表示当前分支在dev上：

git-br-create

你看，Git创建一个分支很快，因为除了增加一个dev指针，改改HEAD的指向，工作区的文件都没有任何变化！

不过，从现在开始，对工作区的修改和提交就是针对dev分支了，比如新提交一次后，dev指针往前移动一步，而master指针不变：

git-br-dev-fd

假如我们在dev上的工作完成了，就可以把dev合并到master上。Git怎么合并呢？最简单的方法，就是直接把master指向dev的当前提交，就完成了合并：

git-br-ff-merge

所以Git合并分支也很快！就改改指针，工作区内容也不变！

合并完分支后，甚至可以删除dev分支。删除dev分支就是把dev指针给删掉，删掉后，我们就剩下了一条master分支：

git-br-rm

真是太神奇了，你看得出来有些提交是通过分支完成的吗？

 下面开始实战。

首先，我们创建dev分支，然后切换到dev分支：

$ git checkout -b dev
Switched to a new branch &#39;dev&#39;
git checkout命令加上-b参数表示创建并切换，相当于以下两条命令：

$ git branch dev
$ git checkout dev
Switched to branch &#39;dev&#39;
然后，用git branch命令查看当前分支：

$ git branch
* dev
  master
git branch命令会列出所有分支，当前分支前面会标一个*号。

然后，我们就可以在dev分支上正常提交，比如对readme.txt做个修改，加上一行：

Creating a new branch is quick.
然后提交：

$ git add readme.txt 
$ git commit -m &quot;branch test&quot;
[dev b17d20e] branch test
 1 file changed, 1 insertion(+)
现在，dev分支的工作完成，我们就可以切换回master分支：
$ git checkout master
Switched to branch &#39;master&#39;

 现在，我们把dev分支的工作成果合并到master分支上：
 
 $ git merge dev
Updating d46f35e..b17d20e
Fast-forward
 readme.txt | 1 +
 1 file changed, 1 insertion(+)
 
 git merge命令用于合并指定分支到当前分支。合并后，再查看readme.txt的内容，就可以看到，和dev分支的最新提交是完全一样的。

注意到上面的Fast-forward信息，Git告诉我们，这次合并是“快进模式”，也就是直接把master指向dev的当前提交，所以合并速度非常快。

当然，也不是每次合并都能Fast-forward，我们后面会讲其他方式的合并。

合并完成后，就可以放心地删除dev分支了

$ git branch -d dev
Deleted branch dev (was b17d20e).

$ git branch
* master




创建与合并分支
阅读: 999256
在版本回退里，你已经知道，每次提交，Git都把它们串成一条时间线，这条时间线就是一个分支。截止到目前，只有一条时间线，在Git里，这个分支叫主分支，即master分支。HEAD严格来说不是指向提交，而是指向master，master才是指向提交的，所以，HEAD指向的就是当前分支。

一开始的时候，master分支是一条线，Git用master指向最新的提交，再用HEAD指向master，就能确定当前分支，以及当前分支的提交点：

git-br-initial

每次提交，master分支都会向前移动一步，这样，随着你不断提交，master分支的线也越来越长：

 当我们创建新的分支，例如dev时，Git新建了一个指针叫dev，指向master相同的提交，再把HEAD指向dev，就表示当前分支在dev上：

git-br-create

你看，Git创建一个分支很快，因为除了增加一个dev指针，改改HEAD的指向，工作区的文件都没有任何变化！

不过，从现在开始，对工作区的修改和提交就是针对dev分支了，比如新提交一次后，dev指针往前移动一步，而master指针不变：

git-br-dev-fd

假如我们在dev上的工作完成了，就可以把dev合并到master上。Git怎么合并呢？最简单的方法，就是直接把master指向dev的当前提交，就完成了合并：

git-br-ff-merge

所以Git合并分支也很快！就改改指针，工作区内容也不变！

合并完分支后，甚至可以删除dev分支。删除dev分支就是把dev指针给删掉，删掉后，我们就剩下了一条master分支：

git-br-rm

真是太神奇了，你看得出来有些提交是通过分支完成的吗？

 下面开始实战。

首先，我们创建dev分支，然后切换到dev分支：

$ git checkout -b dev
Switched to a new branch &#39;dev&#39;
git checkout命令加上-b参数表示创建并切换，相当于以下两条命令：

$ git branch dev
$ git checkout dev
Switched to branch &#39;dev&#39;
然后，用git branch命令查看当前分支：

$ git branch
* dev
  master
git branch命令会列出所有分支，当前分支前面会标一个*号。

然后，我们就可以在dev分支上正常提交，比如对readme.txt做个修改，加上一行：

Creating a new branch is quick.
然后提交：

$ git add readme.txt 
$ git commit -m &quot;branch test&quot;
[dev b17d20e] branch test
 1 file changed, 1 insertion(+)
现在，dev分支的工作完成，我们就可以切换回master分支：

$ git checkout master
Switched to branch &#39;master&#39;
切换回master分支后，再查看一个readme.txt文件，刚才添加的内容不见了！因为那个提交是在dev分支上，而master分支此刻的提交点并没有变：

git-br-on-master

现在，我们把dev分支的工作成果合并到master分支上：

$ git merge dev
Updating d46f35e..b17d20e
Fast-forward
 readme.txt | 1 +
 1 file changed, 1 insertion(+)
git merge命令用于合并指定分支到当前分支。合并后，再查看readme.txt的内容，就可以看到，和dev分支的最新提交是完全一样的。

注意到上面的Fast-forward信息，Git告诉我们，这次合并是“快进模式”，也就是直接把master指向dev的当前提交，所以合并速度非常快。

当然，也不是每次合并都能Fast-forward，我们后面会讲其他方式的合并。

合并完成后，就可以放心地删除dev分支了：

$ git branch -d dev
Deleted branch dev (was b17d20e).
删除后，查看branch，就只剩下master分支了：

$ git branch
* master
因为创建、合并和删除分支非常快，所以Git鼓励你使用分支完成某个任务，合并后再删掉分支，这和直接在master分支上工作效果是一样的，但过程更安全。

Git鼓励大量使用分支：

查看分支：git branch

创建分支：git branch &lt;name&gt;

切换分支：git checkout &lt;name&gt;

创建+切换分支：git checkout -b &lt;name&gt;

合并某分支到当前分支：git merge &lt;name&gt;

删除分支：git branch -d &lt;name&gt;
</code></pre>

<h3 id="toc_12">解决冲突</h3>

<blockquote>
<p>新准备的feature1分支，继续我们的新分支开发：</p>
</blockquote>

<pre><code class="language-none">$ git checkout -b feature1
Switched to a new branch &#39;feature1&#39;

$ git add readme.txt

$ git commit -m &quot;AND simple&quot;
[feature1 14096d0] AND simple

 1 file changed, 1 insertion(+), 1 deletion(-)
 
 到e月刊master分支：
 
$ git checkout master
Switched to branch &#39;master&#39;
Your branch is ahead of &#39;origin/master&#39; by 1 commit.
  (use &quot;git push&quot; to publish your local commits)
  
$ git add readme.txt 
$ git commit -m &quot;&amp; simple&quot;

 这种情况下，Git会无法执行“快速合并”，只能试图把各自的修改合并起来，但这种合并就可能会有冲突，我们试试看
$ git merge feature1

$ git status

Git的用&lt;&lt;&lt;&lt;&lt;&lt;&lt;，=======，&gt;&gt;&gt;&gt;&gt;&gt;&gt;标记出不同分支的内容，我们修改如下后保存：

$ git add readme.txt 
$ git commit -m &quot;conflict fixed&quot;
[master cf810e4] conflict fixed

$ git log --graph --pretty=oneline --abbrev-commit
*   cf810e4 (HEAD -&gt; master) conflict fixed
|\  
| * 14096d0 (feature1) AND simple
* | 5dc6824 &amp; simple
|/  
* b17d20e branch test
* d46f35e (origin/master) remove test.txt
* b84166e add test.txt
* 519219b git tracks changes
* e43a48b understand how stage works
* 1094adb append GPL
* e475afc add distributed
* eaadf4e wrote a readme file

$ git branch -d feature1
Deleted branch feature1 (was 14096d0).
</code></pre>

<h3 id="toc_13">分支策略</h3>

<p>在实际开发中，我们应该按照几个基本原则进行分支管理：</p>

<p>首先，master分支应该是非常稳定的，也就是仅用来发布新版本，平时不能在上面干活；</p>

<p>那在哪干活呢？干活都在dev分支上，也就是说，dev分支是不稳定的，到某个时候，比如1.0版本发布时，再把dev分支合并到master上，在master分支发布1.0版本；</p>

<p>你和你的小伙伴们每个人都在dev分支上干活，每个人都有自己的分支，时不时地往dev分支上合并就可以了。</p>

<p>所以，团队合作的分支看起来就像这样：</p>

<p><img src="./0.png" alt="avatar"><br></p>

<h3 id="toc_14">Bug分支</h3>

<blockquote>
<p>软件开发中，bug就像家常便饭一样。有了bug就需要修复，在Git中，由于分支是如此的强大，所以，每个bug都可以通过一个新的临时分支来修复，修复后，合并分支，然后将临时分支删除。
当你接到一个修复一个代号101的bug的任务时，很自然地，你想创建一个分支issue-101来修复它，但是，等等，当前正在dev上进行的工作还没有提交</p>
</blockquote>

<pre><code class="language-none">$ git status

并不是你不想提交，而是工作只进行到一半，还没法提交，预计完成还需1天时间。但是，必须在两个小时内修复该bug，怎么办？
幸好，Git还提供了一个stash功能，可以把当前工作现场“储藏”起来，等以后恢复现场后继续工作：

$ git stash
Saved working directory and index state WIP on dev: f52c633 add merge
</code></pre>

<p>修复bug时，我们会通过创建新的bug分支进行修复，然后合并，最后删除；
当手头工作没有完成时，先把工作现场git stash一下，然后去修复bug，修复后，再git stash pop，回到工作现场。</p>

<p>git-br-policy
git reset 624f7521ca24e123dadd10665e99314c690d4351 (非本次提交的commitId)</p>

<h4 id="toc_15">不保留本次提交</h4>

<pre><code class="language-none">git reset -hard 624f7521ca24e123dadd10665e99314c690d4351</code></pre>

<h3 id="toc_16">Git 合并代码冲突，冲突恢复到原本冲突状态</h3>

<pre><code class="language-none">选择冲突文件-&gt;解决冲突 -&gt;重新合并</code></pre>

<h3 id="toc_17">Git 创建远程分支</h3>

<pre><code class="language-none">分支-&gt;分支名-&gt;工作副本父节点-&gt;选择分支-&gt;推送到master</code></pre>

<h3 id="toc_18">Git 代码合并错误后，未提交(commit)恢复到合并前</h3>

<pre><code class="language-none">冲突-&gt;重置(贮存)-&gt;重置所有</code></pre>

<blockquote>
<p>注意**要点<br>
将分支合并到主干，分支代码未改变。主干代码为合并后的代码 <br></p>

<h3 id="toc_19">Git 代码合并后，想回退到合并前</h3>

<pre><code class="language-none">情况1：如果合并后，回退，想在合并操作（建议用此操作--不会留下合并记录--&gt;恢复到合并前状态）</code></pre>
</blockquote>

<p>master合并前节点 -&gt;将master重置到这次提交-&gt;强行合并-丢弃所有工作副本修改-&gt;master显示落后版本</p>

<p>-&gt;远程仓库强制覆盖(git push --force)-&gt;合并分支</p>

<p>情况2：如果合并后，commit但是未Push 想重新提交
将master重置到这次提交 -&gt;丢弃所有工作副本修改 
命令: git log 
     git reset --hard 624f7521ca24e123dadd10665e99314c690d4351</p>

<p>情况3： 强制回滚代码至某个节点（删除至某节点所有信息，及分支提交信息）
master合并前节点 -&gt;将master重置到这次提交-&gt;强行合并-丢弃所有工作副本修改
-&gt;提交回滚-&gt;git push --force
注意：如果回滚，会造成分支提交记录全部丢失（建议不使用此方法）
```</p>

<h3 id="toc_20"><center>Git命令</h3>

<pre><code class="language-none">Workspace：工作区
Index / Stage：暂存区
Repository：仓库区（或本地仓库）
Remote：远程仓库
在当前目录新建一个Git代码库
$ git init

# 新建一个目录，将其初始化为Git代码库
$ git init [project-name]
下载一个项目和它的整个代码历史
$ git clone [url]
Git的设置文件为.gitconfig，它可以在用户主目录下（全局配置），也可以在项目目录下（项目配置）。
# 显示当前的Git配置
$ git config --list
编辑Git配置文件
$ git config -e [--global]
# 设置提交代码时的用户信息
$ git config [--global] user.name &quot;[name]&quot;
$ git config [--global] user.email &quot;[email address]&quot;
增加/删除文件
# 添加指定文件到暂存区
$ git add [file1] [file2] ...

 添加指定目录到暂存区，包括子目录
$ git add [dir]

 添加当前目录的所有文件到暂存区
$ git add .

 添加每个变化前，都会要求确认
 对于同一个文件的多处变化，可以实现分次提交
$ git add -p

# 删除工作区文件，并且将这次删除放入暂存区
$ git rm [file1] [file2] ...

 停止追踪指定文件，但该文件会保留在工作区
$ git rm --cached [file]

# 改名文件，并且将这个改名放入暂存区
$ git mv [file-original] [file-renamed]
 提交暂存区到仓库区
$ git commit -m [message]

# 提交暂存区的指定文件到仓库区
$ git commit [file1] [file2] ... -m [message]

 提交工作区自上次commit之后的变化，直接到仓库区
$ git commit -a

# 提交时显示所有diff信息
$ git commit -v

 使用一次新的commit，替代上一次提交
 如果代码没有任何新变化，则用来改写上一次commit的提交信息
$ git commit --amend -m [message]

# 重做上一次commit，并包括指定文件的新变化
$ git commit --amend [file1] [file2] ...
 列出所有本地分支
$ git branch

# 列出所有远程分支
$ git branch -r

 列出所有本地分支和远程分支
$ git branch -a

# 新建一个分支，但依然停留在当前分支
$ git branch [branch-name]

 新建一个分支，并切换到该分支
$ git checkout -b [branch]

# 新建一个分支，指向指定commit
$ git branch [branch] [commit]

 新建一个分支，与指定的远程分支建立追踪关系
$ git branch --track [branch] [remote-branch]

# 切换到指定分支，并更新工作区
$ git checkout [branch-name]

 切换到上一个分支
$ git checkout -

# 建立追踪关系，在现有分支与指定的远程分支之间
$ git branch --set-upstream [branch] [remote-branch]

 合并指定分支到当前分支
$ git merge [branch]

# 选择一个commit，合并进当前分支
$ git cherry-pick [commit]

 删除分支
$ git branch -d [branch-name]

# 删除远程分支
$ git push origin --delete [branch-name]
$ git branch -dr [remote/branch]

# 列出所有tag
$ git tag

 新建一个tag在当前commit
$ git tag [tag]

# 新建一个tag在指定commit
$ git tag [tag] [commit]

 删除本地tag
$ git tag -d [tag]

# 删除远程tag
$ git push origin :refs/tags/[tagName]

 查看tag信息
$ git show [tag]

# 提交指定tag
$ git push [remote] [tag]

 提交所有tag
$ git push [remote] --tags

# 新建一个分支，指向某个tag
$ git checkout -b [branch] [tag]

 显示有变更的文件
$ git status

# 显示当前分支的版本历史
$ git log

 显示commit历史，以及每次commit发生变更的文件
$ git log --stat

# 搜索提交历史，根据关键词
$ git log -S [keyword]

 显示某个commit之后的所有变动，每个commit占据一行
$ git log [tag] HEAD --pretty=format:%s

# 显示某个commit之后的所有变动，其&quot;提交说明&quot;必须符合搜索条件
$ git log [tag] HEAD --grep feature

 显示某个文件的版本历史，包括文件改名
$ git log --follow [file]
$ git whatchanged [file]

 显示指定文件相关的每一次diff
$ git log -p [file]

# 显示过去5次提交
$ git log -5 --pretty --oneline

 显示所有提交过的用户，按提交次数排序
$ git shortlog -sn

# 显示指定文件是什么人在什么时间修改过
$ git blame [file]

 显示暂存区和工作区的差异
$ git diff

# 显示暂存区和上一个commit的差异
$ git diff --cached [file]

 显示工作区与当前分支最新commit之间的差异
$ git diff HEAD

# 显示两次提交之间的差异
$ git diff [first-branch]...[second-branch]

 显示今天你写了多少行代码
$ git diff --shortstat &quot;@{0 day ago}&quot;

# 显示某次提交的元数据和内容变化
$ git show [commit]

 显示某次提交发生变化的文件
$ git show --name-only [commit]

# 显示某次提交时，某个文件的内容
$ git show [commit]:[filename]

 显示当前分支的最近几次提交
$ git reflog

# 下载远程仓库的所有变动
$ git fetch [remote]

 显示所有远程仓库
$ git remote -v

# 显示某个远程仓库的信息
$ git remote show [remote]

 增加一个新的远程仓库，并命名
$ git remote add [shortname] [url]

# 取回远程仓库的变化，并与本地分支合并
$ git pull [remote] [branch]

 上传本地指定分支到远程仓库
$ git push [remote] [branch]

# 强行推送当前分支到远程仓库，即使有冲突
$ git push [remote] --force

 推送所有分支到远程仓库
$ git push [remote] --all
# 恢复暂存区的指定文件到工作区
$ git checkout [file]

 恢复某个commit的指定文件到暂存区和工作区
$ git checkout [commit] [file]

# 恢复暂存区的所有文件到工作区
$ git checkout .

 重置暂存区的指定文件，与上一次commit保持一致，但工作区不变
$ git reset [file]

# 重置暂存区与工作区，与上一次commit保持一致
$ git reset --hard

 重置当前分支的指针为指定commit，同时重置暂存区，但工作区不变
$ git reset [commit]

# 重置当前分支的HEAD为指定commit，同时重置暂存区和工作区，与指定commit一致
$ git reset --hard [commit]

 重置当前HEAD为指定commit，但保持暂存区和工作区不变
$ git reset --keep [commit]

# 新建一个commit，用来撤销指定commit
# 后者的所有变化都将被前者抵消，并且应用到当前分支
$ git revert [commit]

 暂时将未提交的变化移除，稍后再移入
$ git stash
$ git stash pop
 生成一个可供发布的压缩包
$ git archive</code></pre>


</body>

</html>
