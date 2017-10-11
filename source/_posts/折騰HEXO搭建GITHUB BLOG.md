---
title: 折騰HEXO搭建GITHUB BLOG 
tags: 折腾、hexo、GitHub
grammar_cjkRuby: true
---

> 根据网上搜索到教程，折腾了一天，写下此文以记录一个小白瞎折腾的历程。
# 安装nvm
操作系统为Ubuntu 16.04，此前已装好GIT、NODEJS，按照此教程的方法，还得nvm安装Node.js 
教程1：[enter description here][1]
但是这个教程里没说明要怎么安装nvm呀（黑人问号脸？？？）
什么 pip \ apt-get \ wget \ curl...所有目前我知道的安装命令都试了个遍，就是无法安装nvm。
        所以就只有继续问度娘了（暂时去不了谷爷家），找了几篇安装nvm的教程，最后在这一教程里找到成功安装nvm的方法。
		wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.33.0/install.sh | bash
		教程2：[enter description here][2]
成功安装nvm后就可以继续装逼下去了，按照教程1继续安装好Node.js，我直接用命令安装 “ nvm install node"，而不是选择版本号安装，这样它会安装当前最新版本的。

## 安装Hexo
> 接下来我们需要用Hexo初始化一个博客，然后更改一些自定义的配置，或者加上自己喜欢的主题，写上第一篇文章，然后发布到自己的个人Github网站(username.github.io)。

*起初按照教程初始化一个博客时会出现我看不懂的报错，但博客是初始化“成功的”，可以看到文件夹，里面相应的文件也一并都有。输入命令测试 hexo s ，报错。
*后来想想会不会加个SU权限会好一点，然后就重新初始化一个博客，使用" sudo hexo init filename "，这下没报错了。往后的操作都加“sudo”来进行。"sudo gedit _config.yml" 来编辑配置文件，测试成功。

### Markdown语法
进行到上面那个步骤内心是十分欢喜的，毕竟离成功又近了一步。
待看到试着发布自己第一篇博文时，说到按Markdown语法编写md文件，一下子懵圈了，Markdown语法是什么鬼？我是小白呀，我什么都不懂呀，所以又只能靠度娘了。最后找到了一个[在线编辑器][3]。此文就是在编辑器中编写的。
看教程，**粗体字是不是这样？**
*斜体字是这样的？*
--那这样会不会加个删除线--
看来是不会。。。

好吧，先这样，我要试试把这篇文发出去。



好吧，发出去一次。这是第二次编辑。
先说说这个在线编辑器吧，如果要保存到本地还得先绑定第三方存储。
所以我只能全选再复制粘贴。T_T



#### 安装hexo-deployer-git自动部署发布工具
按照教程一步一步来，却总是报错。后来在知乎看到有人也在问这个问题，原来是我没把这台电脑的SSH加到githubu上==#
将SSH加进去后终于成功了。
接下来就是生成静态网页文件发布至我们的Github pages 中，
照教程那个三连发的命令 “$ hexo clean && hexo g && hexo d”
老是报错，所以我又只能一个一个命令输入了。
好在，最后成功了。
在地址栏输入：verzzz.github.io 就能打开博客了。

##### The End
折腾了一天，结合网上众多教程终于搞定了。
过程中好多命令都看不懂，只能依样画葫芦，也因为不懂，走了好多弯路，浪费了好多时间。
好吧，以后再继续折腾吧。
折腾不止，生命不息。

***
To be Continue
***


  [1]: http://www.jianshu.com/p/4eaddcbe4d12
  [2]: http://blog.csdn.net/aym_fuhong/article/details/53046585?locationNum=1&fps=1
  [3]: http://markdown.xiaoshujiang.com/
