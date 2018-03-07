---
title: Windows下hexo+githubpage搭建
date: 2018-03-07 10:46:28
desc: Lorem ipsum dolor sit amet, consectetur.
---
目前静态网站有很多搭建方法，jekyll+githubpage，hexo+githubpage我采用的是hexo+githubpage，因为jekyll好麻烦啊，泪～～～ 
 
# 环境搭建

# 安装git

1. 下载：下载windows版本的github  
下载地址：[github-windows](https://git-scm.com/download/win)  
  
2. 安装：双击安装，一路next。

# 安装node.js
1. 下载：官网下载最新版的node.js  
下载地址：[node.js](https://nodejs.org/zh-cn/download/)  
2. 安装：双击安装，一路next

# 安装hexo
打开git bash/git shell  
输入: 
> npm install hexo-cli -g  

安装过后输入hexo-v，出现以下信息，则表示安装成功
>hexo: 3.6.0  
hexo-cli: 1.1.0  
os: Windows_NT 6.1.7601 win32 x64  
http_parser: 2.7.0  
node: 8.9.4  
v8: 6.1.534.50  
uv: 1.15.0  
zlib: 1.2.11  
ares: 1.10.1-DEV  
modules: 57  
nghttp2: 1.25.0  
openssl: 1.0.2n  
icu: 59.1  
unicode: 9.0  
cldr: 31.0.1  
tz: 2017b  

# 初始化blog
进入准备创建的blog目录，打开git bash/git shell，输入以下命令初始化：
>hexo init yourblogname

自动产生blog的目录，本地blog已建好，输入：
> cd yourblogname  
> hexo server

浏览器输入127.0.0.1:4000或者是localhost:4000即可访问。

#换theme
自带的皮肤略丑，可以去[官网](https://hexo.io/themes/)挑选自己喜欢的皮肤，当然有能力的可以自己做。根据作者的github教程，一般是：
>git clone 作者的theme.git themes/* 

将_config.yml中的thems: landscape 改为*  
刷新即可看到修改结果
# 部署
1. 新建仓库：  
在你的github中新建同你github用户名相同的仓库，setting中可看见你的githubpage地址
2. 在_config.yml中配置git服务器：
>deploy:  
>>  type: git  
    repo: git@server:/home/git/blog.git  
    branch: master  

3. 输入:
>hexo g  
>hexo d

部署成功，打开地址即可访问
这里附上我的[blog地址](https://illusionmia.github.io/)
