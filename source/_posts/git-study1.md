---
title: git_study1
date: 2019-10-13 19:18:13
tags: git study
---

## Git 学习1：Git Bsaics -Getting a Git Repository

### 初始化你的仓库

1. 进入项目目录

2. ~~~ git
   $ git init
   $ git add * //加入文件
   $ git add LICENSE
   $ git conmmit -m 'initial project version'
   $ git status //查看当前项目的管理状态
   报错pathspec 'xxx' did not match any files时需要手动创建该文件
   ~~~

### 克隆远程仓库

1. ~~~ git
   git clone <url>
   ~~~

### 忽略某些临时文件

~~~git
$ cat .gitignore //创建被忽略的文件列表,window进入编辑器编辑
	*.[oa]
	*~
	git会忽略所有结尾带有.o . a ~ 的文件
~~~



### git 常用命令

~~~ git
$ 
~~~