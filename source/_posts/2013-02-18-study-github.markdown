---
layout: post
title: "study github"
date: 2013-02-27 17:01
comments: true
categories: 
---
#准备工作

1. 在[https://github.com/](https://github.com)中注册一个帐号。
2. 下载一个git,参考一篇[git入门指南](http://rogerdudler.github.com/git-guide/index.zh.html)。

参考资料：
[如何高效利用GitHub](http://www.yangzhiping.com/tech/github.html)

如何使用GitHub写博客
--------------------
可以在Github上快速搭建一个基于jekyll的博客系统

* Jekyll：参考[告别wordpress，拥抱jekyll](http://www.yangzhiping.com/tech/wordpress-to-jekyll.html)	
* [利用Jekyll搭建个人博客](http://www.mceiba.com/develop/jekyll-introduction.html)
* Octopress：参考Ruby开源项目介绍(1)：[octopress——像黑客一样写博客](http://www.yangzhiping.com/tech/octopress.html)

由于我的系统平台是WindowXP,所以参考了 [5步搭建博客](http://pezy.github.com/about/)
####第一步：####
注册GitHub,注册完后，配置Git。这里没有谈到添加SSH密钥，可参考[Generating SSH Keys](https://help.github.com/articles/generating-ssh-keys)

*__注意：默认的22号端口有可能被占用或阻止，可建立一个config文件进行设置__*
	Host github.com
	User username@email.com
	Port 443
	Hostname ssh.github.com
请把`username@email.com`换成你的GitHub注册邮箱。

*single asterisks*

_single underscores_

**double asterisks**

__double underscores__
![Alt text](https://help.github.com/assets/help/logo-help-cc8a5cc88bc35f6b6431f44ac7a1c9bd.png)

####第二步：####
搭建Ruby环境
*__注意：我在我的机子上使用Git Bash无法启动ruby，因此我只好单独启动Ruby来完成第二、三、四步。__*
**可通过`我的电脑/属性/高级/环境变量`添加Ruby的路径，解决此问题**
####第三步：####
安装Octopress框架
####第四步：####
写一篇简单的blog进行测试。jekyll采用markdown格式的轻量级标记语言。
关于markdown语言可参考[Markdown 语法说明](http://wowubuntu.com/markdown/)。</br>
*__注意：这步可能出现GBK编码错误。__*

####第五步####
最后一步，要把本地文件部署到GitHub服务器上去。


__Create a new repository on the command line__
	touch README.md
	git init
	git add README.md
	git commit -m "first commit"
	git remote add origin git@github.com:cpq37/cpq37.github.com.git
	git push -u origin master
__Push an existing repository from the command line__
	git remote add origin git@github.com:cpq37/cpq37.github.com.git
	git push -u origin master