---
title: "About"
date: 
lastmod:  
menu: "main"
weight: 50

# you can close something for this content if you open it in config.toml.
comment: false
mathjax: false
---

GitHub Pages 是一个静态站点托管服务，直接将个人、组织或项目的页面托管于 GitHub 库或仓库 (repository) 中。
Hugo 是一个用 Go 语言编写的静态站点生成器，它针对速度、易用性和可配置性进行了优化，快速灵活。

## error大集合


*error: 源引用规格 master 没有匹配*

*error: 推送一些引用到 'github.com:‘*

解决： 

    git commit -m ""


*You've added another git repository inside your current repository.*

解决： 

    git rm -r --cached log  //删除对log的track

    git submodule add url //添加log到子目录

我这里是 git submodule add --depth=1 https://github.com/xianmin/hugo-theme-jane.git themes/jane   --depth 



*error: build and deploy all jobs have failed*

解决：生成编译文件

    hugo -d docs

再在仓库的setting中选择docs

该方式的优点是将源文件与编译文件分开



*fatal: unable to access "...github"*

解决：用SSH方式连接，不要用HTTP。

同时注意SSH是否已经与另一个账号连接，若有则需要删除。



# 其他命令
git command
    
    git remote -v //查看远程仓库
    
    git init //初始化仓库
    
    git clean
    
    git add .
    
    git commit -m "doc"
    
    git push origin master



hugo command

    hugo new site site_name

可得到如下目录结构

personal-site

├── archetypes

├── config.toml   //Hugo的配置文档

├── content       //存放所有Markdown格式的文章

├── data

├── layouts

├── static

└── themes        //存放下载的主题

编译网站

    hugo -d

会在/public中生成网页文件

