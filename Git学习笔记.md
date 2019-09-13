# Git学习笔记

## Git简介

## 安装Git

## 创建版本库

初始化

git init

# 文件添加到版本库

git add file.txt

git commit -m "add a file"

##管理版本

## 回退本版本

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

