# 概述
 - 产品定义：ynote，一个专注于开源框架（OF）的内容管理平台（CMS），为OF作者提供代码托管,维护最完整、准确、高效的文档，最大限度推广OF。为OF读者提供基于实用和原理的OF的文档，最大限度git remote 了解OF，他提供最佳OFs建议。为作者和读者维护评论，交流
 - 本文目标。分析当前相似产品使用技术，复用、优化，提出ynote的技术方案
 - 技术要点。git+wiki+社交
 - 技术细节：目录，批注，审阅
 - 关键字：yiki，ynote，源笔记
# 产品PK
 | 产品 | 特点 | 借鉴之处 |
 | ------ | ------ | ------ |
 | Gogs | Go语言，开源，[JIAHUA CHEN](https://github.com/Unknwon) | Jenkins  |
 | gollum | RB语言，开源，authentication，Gollum不支持kramdown的高级用法，跟GitHub上的Wiki差不多，只支持最基本的Markdown语法， 不要试图折腾格式 | authentication用户鉴权 |
|pandao   |  一个基于github的管理开源的，md编辑器，Editor.md 建立在众多优秀的开源组件基础之上，遵循和使用 MIT License 开源协议，无论个人还是公司，都可以免费自由使用。更新于 2015-06-09， |   |   |

## MD-ide
### Atom
Atom 是Github 专门为程序员推出的一个跨平台的开源的文本编辑器。写作神器，这个编辑器完全是使用Web技术构建的(基于Node-Webkit)。启动速度快，提供很多常用功能的插件和主题，可以说Atom已经足以胜任“半个IDE”了。Atom比其他文本编辑器更有效率。

打开settings界面，点击左侧栏的Install按钮。然后在搜索框中输入关键字markdown，点击右侧packages开始搜索
必备插件：
使用以下插件（都可以在 Settings > Install 里面找到）：
markdown-preview：编辑实时预览插件，Atom 官方出品
language-markdown：提供 Github Flavored Markdown 等 MD 高亮支持
markdown-scroll-sync：将 markdown-preview 的编辑区和预览区同步滚动
markdown-writer：方便管理图片、链接等
markdown-table-formatter：格式化表格
图片粘贴(markdown-image-paste)
activate-power-mode:动画编码
git-plus：git 操作的插件。与github深度契合。完美无缺。

如何使用？ 按ctrl + shift + p 弹出搜索框，然后搜索markdown preview，然后点击enter即可使用.侧边栏的keybindings，在弹出界面的搜索框中输入markdown，就能找到所有与markdown有关的快捷键

### Haroopad

2013年开发完成，然后一直没有更新？
官网：
http://pad.haroopress.com/

作为使用人员进入：
http://pad.haroopress.com/user.html

github地址：
https://github.com/rhiokim/haroopad/

国际化，跨平台，可以在windows mac linux上使用！

#### REF

http://blog.csdn.net/wangshubo1989/article/details/53007104
 ### QA
 word,html 如何快速转化为md

 node-webkit是个什么鬼？



# GitWeb
table

## GitBooK
这个工具链 (GitBook) 是一个使用 Git 和 Markdown 来构建书籍的工具，是开源并且完全免费的，它的源码可以在 [GitHub](https://github.com/GitbookIO/gitbook) 上获取

GitBook.com 是一个使用工具链来创建和托管书籍的在线平台 (www.gitbook.com)。

成立于2014.9于法国,250k user。150k books，
20M vistors/Month

nodejs,注意：在我的实验中，gitbook init 只支持两级目录！
下载
 [gitbook](https://github.com/GitbookIO/editor) 编辑器，做到所见即所得的编辑，如下图所示：

[插件](http://www.chengweiyang.cn/gitbook/plugins/README.html)

[android-bookmarks](https://www.gitbook.com/book/bookmarks/android-bookmarks/details)

### 基于gitbook建立自己的GitWeb
Powered by Jekyll, theme by Matt Harzewski
### ref
[gitbook手册](https://chrisniael.gitbooks.io/gitbook-documentation/content/#)

[gitbook简明教程](http://www.chengweiyang.cn/gitbook/basic-usage/README.html)


## Github Pages
GitHub Pages 可以为你或者你的项目提供介绍网页，它是由 GitHub 官方托管和发布的。你可以使用 GitHub 提供的页面自动生成器。也可以做个人博客，是个轻量级的博客系统，没有麻烦的配置。使用标记语言如Markdown，不需自己搭建服务器，还可以绑定自己的域名。
GitHub Pages为了提供对HTML内容的支持，选择了Jekyll作为模板系统，Jekyll是一个强大的静态模板系统，作为个人博客使用，基本上可以满足要求，也能保持管理的方便。

Github Pages - 官方配置指南
  工作流：写markdown文件，提交大屏仓库，Pages调起Jekyll，把md文件编译成html，浏览器可以查看了
Whenever you commit to this repository, GitHub Pages will run Jekyll to rebuild the pages in your site, from the content in your Markdown files.

如何http://www.cnblogs.com/lijiayi/p/githubpages.html

## Gogs
Gogs 是一款极易搭建的自助 Git 服务. 目标是打造一个最简单、最快速和最轻松的方式搭建自助 Git 服务。使用 Go 语言开发使得 Gogs 能够通过独立的二进制分发，并且支持 Go 语言支持的 所有平台，包括 Linux、Mac OS X、Windows 以及 ARM 平台。Go Web 框架采用Macaron

- [官网](https://gogs.io/)

- [Gogs最近更新很慢，gogs还会继续开发吗？](Gogs最近更新很慢，gogs还会继续开发吗？)

## Gollum
gollum 是 GitHub 的 Wiki 程序, 极简主义 + Git + 原生 Markdown 支持, 很酷, 但是默认引擎不支持用中文作为标题, 这个就很操蛋了, 换了新的引擎虽然可以使用中文标题, 但是仍然不支持中文搜索——不过这个问题我已经通过修改源码的形式解决, 并且提交PR给仓库, 也许会有被合并的一天(关于gollum的几个项目社区活跃度都很低).

我做了一个实现支持中文的 gollum 一键部署 Docker 镜像, 内置了所有 gollum 支持格式依赖, 开箱即用, 有兴趣的可以试试: BlackGlory/docker-rugged-gollum.

剩下的唯一问题就是 gollum 没有自带用户鉴权, 而且维护者们也不愿意添加此功能, 需要用户自己搞定用户鉴权. arr2036/omnigollum是一个给 gollum 加上 omniauth 的项目, 但已经多年没有维护代码了, 有待 review.

### ref
[基于Git的维基管理：gollum](http://www.yangzhiping.com/tech/gollum.html)

[gollum:轻量级的wiki系统](http://www.bjt.name/2015/10/gollum)

[markdown + git 最适合程序员的wiki系统：gollum](http://www.open-open.com/lib/view/open1422014636421.html)

[gollum:给wiki插上git的翅膀](http://www.jianshu.com/p/9c35812b9bae)

## markdown
### neditor
马云
### Cmd Markdown
Cmd Markdown 发布第九次更新 --- 写在侧边 https://www.zybuluo.com/ghosert/note/41556

## GitWeb
## 产品pk
### 马云
奥思网络科技
https://gitee.com
gvp：最有价值的开源项目
码云于2013年正式推出，由开源中国基于 Gitlab 所开发，我们在 Gitlab 的基础上做了大量的改进和定制开发，致力于为国内开发者提供优质稳定的托管服务。目前已成为国内最大的代码托管系统。
##
# 技术方案

# 产品形态
cms，电子出版：编写
工具类：confluence
帮助程序员出书

工具：

内容(2c)：汉化，厚薄转化
read the docs:CodeIgniter

服务
## 百度文库
## 微信读书
tts语音识别
## 得到
