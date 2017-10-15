# 1.概述
 - 产品定义1：ynote，一个专注于开源框架（OF）的内容管理平台（CMS），为OF作者提供代码托管,维护最完整、准确、高效的文档，最大限度推广OF。为OF读者提供基于实用和原理的OF的文档，最大限度git remote 了解OF，他提供最佳OFs建议。为作者和读者维护评论，交流
 - 产品定义2：ynote，类似于gitbook和readthedoc的web应用，帮助程序员方便地写技术文档
 - 本文目标。分析当前相似产品使用技术，复用、优化，提出ynote的技术方案
 - 技术要点。git+wiki+社交
 - 技术细节：目录，批注，审阅
 - 关键字：yiki，ynote，源笔记
# 1.MD-IDE
## Atom
Atom 是Github 专门为程序员推出的一个跨平台的开源的文本编辑器。写作神器，这个编辑器完全是使用Web技术构建的(基于Node-Webkit)。启动速度快，提供很多常用功能的插件和主题，可以说Atom已经足以胜任“半个IDE”了。Atom比其他文本编辑器更有效率。

打开settings界面，点击左侧栏的Install按钮。然后在搜索框中输入关键字markdown，点击右侧packages开始搜索
必备插件：
使用以下插件（都可以在 Settings > Install 里面找到）：
- 预览：markdown-preview（自带Atom）markdown-preview< markdown-preview-plus < markdown-preview-enhanced（主题preview+toc）
- 代码着色：language-markdown：代码着色，还提供了快捷的代码片段生成等功能
- Github Flavored
- markdown-scroll-sync：将 markdown-preview 的编辑区和预览区同步滚动
- markdown-writer：方便管理图片、链接等
- markdown-table-formatter：格式化表格
- 图片粘贴(markdown-image-paste)
- activate-power-mode:动画编码
- git-plus：git 操作的插件。与github深度契合。完美无缺。

如何使用？

侧边栏的keybindings，在弹出界面的搜索框中输入markdown，就能找到所有与markdown有关的快捷键


预览功能： ctrl + shift + p --> 搜索markdown preview；ctrl + shift + m
TOC功能： ctrl + shift + p --> 输入 TOC 即可
## Haroopad
2013年开发完成，然后一直没有更新？功能确实很强大，专门为markdown而生，语法提示，插入时间之类都很方便，这写都是atom目前没有的
官网：http://pad.haroopress.com/

作为使用人员进入：
http://pad.haroopress.com/user.html

github地址：
https://github.com/rhiokim/haroopad/

国际化，跨平台，可以在windows mac linux上使用！
## editor.md
Editor.md 是一个可嵌入的开源 Markdown 在线编辑器组件，你可以很方便用在浏览器、NW.js（Node-webkit）等地方，基于CodeMirror、jQuery 和 Marked 构建。
http://www.oschina.net/p/editor-md
非常感谢Editor.md的开源，因为有你我才能搭建一款比较完美的使用markdown写博客的网站 http://yaokwok.com 不过看到Editor两年没更新了有点小小是失落，希望开源永恒！ #Editor.md#
在线演示

https://pandao.github.io/editor.md/examples/index.html

## amWiki
amWiki 是一款由 JS 开发、依赖 Atom 或 Nodejs-Npm 的 Markdown 轻量级前端化开源文库系统
amWiki 可以同时在 Atom 编辑器和 nodejs npm 的命令行两个平台工作，两个平台的工作相互独立，但所创建的文库却可以相互共用
（PS：对这两个平台的依赖都是编辑需求而不是服务器需求，amWiki 创建的文库是纯静态 html，可以布置到任意服务器）
4月份开始弄的。2人开发的
[amWiki](https://github.com/TevinLi/amWiki/blob/master/README.md)
[官网](https://amwiki.org/)
## Cmd Markdown
  在线编辑，批注功能都很好，就是不开源。。。
我是作业部落的主要开发者张佳伟，
Cmd Markdown 发布第九次更新 --- 写在侧边 https://www.zybuluo.com/ghosert/note/41556

## other
- MarkdownPad：只有windowns版本，2017年还有维护,免费版用户限制比较多，不过基本功能都有了

- MdCharm：Win和Linux平台
官网 http://www.mdcharm.com/
开源,最新发布14-Otc-2013，不再维护，out了？
- everedit	Win平台，$35，全能型的编辑器，Markdown只是其中部分功能
- stackedit	体验了一下，作为在线编辑器，确实不错，第一次使用需要缓存较多文件，会比较慢，后面就好了使用LocalStorage保存，不过没关系可以导出MD和HTML，PDF需要付费，$5/year(可以通过Chrome的导出到PDF弥补)，另外可以绑定Google Drive和Dropbox(付费用户)，我倒其实蛮care这些东西的源头的， 不知道stackedit是不是第一家， 但至少我看到stackedit是第一家， 而且最重要的是stackedit是开源的。 看着这些跟stackedit长的那么像的编辑器们， 当然我承认排名第一的确实更好， 你们向先行的开发者们致敬了么?
stackEdit支持边写文档边加批注，方便随时添加todo提醒，类似”这里要加个图片“。

- 马克飞象	：专为印象笔记打造的Markdown编辑器 ——这个主要是为印象笔记服务的了。
-neditor:马云


## REF
// TODO
[Haroopad--最好用的markdown编辑器](http://blog.csdn.net/wangshubo1989/article/details/53007104)
[作业部落出品的Cmd Markdown 编辑阅读器怎么样？有没有同类型的更好的呢？](https://www.zhihu.com/question/23962028)
[Atom：优雅迷人的编辑神器](http://www.jianshu.com/p/b4c8479cfaa5)
[Atom在系统下安装activate-power-mode插件问题？](http://www.jianshu.com/p/b4c8479cfaa5)：重复多试几次就好了
[如何评价 GitHub 发布的文本编辑器 Atom？](https://www.zhihu.com/question/22867204)
[使用Atom打造无懈可击的Markdown编辑器](http://www.cnblogs.com/fanzhidongyzby/p/6637084.html)
[新编码神器Atom使用纪要](https://www.jeffjade.com/2016/03/03/2016-03-02-how-to-use-atom/)

[开源在线 Markdown](http://pandao.github.io/editor.md/)
[Cmd Markdown](https://www.zybuluo.com/ghosert/note/41556) 批注：批注社交功能很好，但是貌似是作业部落的不开源哦

# HTML-IDE
在CSDN、cnblogs等博客平台上写的，不过个人觉得界面设计、页面效果比较low，不符合我的审美观
## Jekyll
Jekyll 是一个为博客设计的静态网站生成器，也可以用于个人、项目或组织的网站构建。可以认为，Jekyll 是一个基于文件的内容管理系统（CMS）。它使用 Ruby 编写，通过 Markdown 和 Liquid 模板生成内容。
有了 Jekyll 这类静态博客生成工具，我们不再需要使用动态语言开发和运行后端程序（如：Wordpress 和 Drupal 等），而只是需要一个静态 HTTP Server。甚至，在有了 GitHub Pages 后，连服务器资源都可以省去。当然，静态网站的好处不止是节省资源，还有安全、速度、扩展性等考虑。具体可以阅读文章：https://www.netlify.com/blog/2016/05/18/9-reasons-your-site-should-be-static。
使用 HEXO 在多台电脑上发布博客，操作起来并不是那么方便，果断就转到了 Jekyll 上
Jekyll 是一个简单的博客形态的静态站点生产机器。它有一个模版目录，其中包含原始文本格式的文档，通过 Markdown （或者 Textile） 以及 Liquid 转化成一个完整的可发布的静态网站，你可以发布在任何你喜爱的服务器上。Jekyll 也可以运行在 GitHub Page 上，也就是说，你可以使用 GitHub 的服务来搭建你的项目页面、博客或者网站，而且是完全免费的

　使用 Jekyll 搭建博客之前要确认下本机环境，Git 环境（用于部署到远端）、Ruby 环境（Jekyll 是基于 Ruby 开发的）、包管理器 RubyGems
　　如果你是 Mac 用户，你就需要安装 Xcode 和 Command-Line Tools了。下载方式 Preferences → Downloads → Components。
Jekyll 是一个免费的简单静态网页生成工具，可以配合第三方服务例如： Disqus（评论）、多说(评论) 以及分享 等等扩展功能，Jekyll 可以直接部署在 Github
使用了 Jekyll 你会发现如果你想使用多台电脑发博客都很方便，只要把远端 github 仓库里的博客 clone 下来，写文章后再提交就可以了，Hexo 由于远端提交的是静态网页，所有无法直接写 Markdown 的文章。
   Jekyll的核心其实就是一个基于ruby语言的文本的转换引擎，用你最喜欢的标记语言写文档，可以是Markdown、Textile或者HTML等等，再通过layout将文档拼装起来，根据你设置的URL规则来展现，这些都是通过严格的配置文件来定义，最终的产出就是web页面。

## HEXO
使用 HEXO 在多台电脑上发布博客，操作起来并不是那么方便
配置环境
安装Node（必须）
作用：用来生成静态页面的 到Node.js官网下载相应平台的最新版本，一路安装即可。
安装Git（必须）
作用：把本地的hexo内容提交到github上去. 安装Xcode就自带有Git，我就不多说了。
申请GitHub（必须）
作用：是用来做博客的远程创库、域名、服务器之类的，怎么与本地hexo建立连接等下讲。 github账号我也不再啰嗦了,没有的话直接申请就行了，跟一般的注册账号差不多，SSH Keys，看你自己了，可以不配制，不配置的话以后每次对自己的博客有改动提交的时候就要手动输入账号密码，配置了就不需要了，怎么配置我就不多说了，网上有很多教程。
## http://octopress.org/
## https://ghost.org/
## REF
[采用Jekyll+GitHub Pages搭建的个人博客站点](https://github.com/stidio/stidio.github.io)：有统计，但是没有评论？
[深入 Jekyll](https://github.com/stidio/stidio.github.io)
[HEXO搭建个人博客](http://baixin.io/2015/08/HEXO%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/)




 ### QA
 word,html 如何快速转化为md

 node-webkit是个什么鬼？

 Word 转化为md



# GitWeb
## 概述
| 产品 | 特点 | 借鉴之处 |
 | ------ | ------ | ------ |
 | Gogs | Go语言，开源，[JIAHUA CHEN](https://github.com/Unknwon) | Jenkins  |
 | gollum | RB语言，开源，authentication，Gollum不支持kramdown的高级用法，跟GitHub上的Wiki差不多，只支持最基本的Markdown语法， 不要试图折腾格式 | authentication用户鉴权 |
|pandao   |  一个基于github的管理开源的，md编辑器，Editor.md 建立在众多优秀的开源组件基础之上，遵循和使用 MIT License 开源协议，无论个人还是公司，都可以免费自由使用。更新于 2015-06-09， |   |   |
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

## 北半球
北半球是由个人开发，以分享技术知识为主的知识分享社区，在这里你可以：

使用Markdown在线制作书籍
在线阅读其他用户制作的技术书籍
通过讨论区和其他人一起交流、互相讨论
书籍制作成pdf、epub、mobi电子书格式

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
## 马云
奥思网络科技,类似于coding
https://gitee.com
gvp：最有价值的开源项目
码云于2013年正式推出，由开源中国基于 Gitlab 所开发，我们在 Gitlab 的基础上做了大量的改进和定制开发，致力于为国内开发者提供优质稳定的托管服务。目前已成为国内最大的代码托管系统。
## 简书
简书首页写着“一个基于内容分析的社区”，也就是啥啥啥文章都有，不只是技术博客
[简书有一款牛逼的markdown写作工具你知道吗](http://www.jianshu.com/p/be0b5a31aca6)
## 蚂蚁笔记
open source alternative to Evernote
蚂蚁笔记，有极客范的云笔记！
前所未有的文档体验，近乎完美的平台覆盖，支持团队协同，企业级私有云

蚂蚁笔记 = 笔记 + 博客 + 协作 + 私有云
## http://www.ecshop.com/
## REF
[基于Git的维基管理：gollum](http://www.yangzhiping.com/tech/gollum.html)

[gollum:轻量级的wiki系统](http://www.bjt.name/2015/10/gollum)

[markdown + git 最适合程序员的wiki系统：gollum](http://www.open-open.com/lib/view/open1422014636421.html)

[gollum:给wiki插上git的翅膀](http://www.jianshu.com/p/9c35812b9bae)

[个人知识管理公开方案的摸索WIKI](https://www.blackglory.me/exploring-the-open-program-of-personal-knowledge-management/)
# 讨论备忘
## 工具
cms，电子出版：编写
工具类：confluence 帮助程序员出书
工具：

## 内容(2c)
汉化，厚薄转化
read the docs:CodeIgniter

## 服务
 百度文库
 微信读书
  tts语音识别
 得到app
