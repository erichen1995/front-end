## git基本概念
git是版本控制软件
github:用来托管项目的仓库,网站.

## Git文件的三种状态
你的文件可能 处于其中之一： 已提交（committed）、已修改（modified） 和 已暂存（staged）。

## Git项目的三个阶段
 Git 项目拥有三个阶段：工作区、暂存区以及 Git 目录

## Git文件暂存,提交,覆盖
![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200929135808.png)

## Git文件状态转换过程
![](https://cdn.jsdelivr.net/gh/erichen1995/MarkdownPhotos@master/img/20200929135822.png)


##  Git diff
比较工作目录中当前文件和暂存区域快照之间差异,也就是修改之后还没暂存起来的内容.
 `git diff --staged` 命令, 这条命令将比对已暂存 文件与最后一次提交的文件差异.

## 从Git中移除文件
`rm xxx.md`
`git rm xxx.md`
如果要删除之前修改过或已经放到暂存区的文件，则必须使用 强制删除选项 -f（译注：即 force 的首字母）

## 从Git仓库移除,但是不动当前目录
`git rm --cached README`

## 撤销commit操作
这个命令会将暂存区中的文件提交.如果自上次提交以来你还未做任何修改,那么快照会保持不变，而你所修改的只是提交信息.
```git
git commit -m 'initial commit' //第一次提交
git add forgotten_file			//添加忘了的目录
git commit --amend            //第二次提交
```
最终只会有一个提交——第二次提交将代替第一次提交的结果。

## Git fetch \<remote>
这个命令会访问远程仓库，从中拉取所有你还没有的数据。 执行完成后，你将会拥有那个远程仓库中所有分支 的引用，可以随时合并或查看。

## git push -u 的有什么意义
git push [-u | --set-upstream ] your-fetch 成功推送,添加上游(跟踪)引用.

## Git修改仓库地址
git remote set-url [you-url] 修改仓库地址

## GIt修改当前分支名
git branch -M master 修改当前分支名

## git Merge
????