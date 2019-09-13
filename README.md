# Git学习笔记

## Git简介

目前最先进的分布式版本控制系统，Linux之父林纳斯·托瓦兹为了管理Linux内核源代码开发了Git

## 创建版本库

初始化

git init

# 文件添加到版本库

git add file.txt

git commit -m "add a file"

## 管理版本

### 查看版本

git log

git log --pretty=oneline

按q退出查看（通Vim或Linux操作方式）

### 回退到相应版本

方式一：git reset --hard HEAD^

版本解释：

当前版本：HEAD

上一个版本HEAD^或HEAD~1

上上个版本HEAD^^或HEAD~2

git reset --hard HEAD^

方式二：git reser --hard commitid

例：git reset --hard a1191d6f48c3d14f796057cc3244de04b977409b

## 工作区、暂存区

工作区：即工作目录

版本库：工作区隐藏目录.git

- index是暂存区
- HEAD是指向master的指针

工作流程：

- git add提交文件到暂存区
- git commit把暂存区内容提交到当前分支

## 撤销操作

从工作区撤销

git checkout -- readme.txt

从暂存区撤销

git reset HEAD readme.txt

## 克隆仓库

git clone https://github.com/junstudys/learngit.git

## 推送远程仓库

git push -u origin master（第一次推送远程库为空需加-u参数）

git push origin master

## 分支git管理

创建分支

git checkout -b feature

切换分支

git checkout master

合并分支:feature分支合并到master

git merge feature

## 多人协作

查看远程库信息

git remote

git remote -v

推送分支

git push origin master

## 更新远程库

使用git fetch更新，相当于是从远程获取最新版本到本地，不会自动merge

git fetch origin master 

git log -p master..origin/master 

git merge origin/master  