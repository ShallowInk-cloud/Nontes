# Git 理论核心

## Git流程

**git本地有有三个工作区域  工作目录(Working Directory)  、  暂存区(Stage/Index)  、 资源库(Repository或Git Directory)。如果在加上远程的git仓库(Remote Directory)就可以分为四个工作区域。文件在这四个区域之间的转换关系如下：**

==本地上传==

```
Working Directory --"git add files"--> Stage(Index) --"git commit"-->  History  --"git push" -->  Remote Directory
```
==下载到本地==

```
Remote Directory  --"git pull"--> History  --"git reset"-->  Stage(Index)  --"git checkout"-->  Working Directory
```

- Working Directory: 工作区，就是你平时存放项目代码的地方
- Index/Stage:暂存区，用于临时存放你的改动，事实上它只是一个文件，保存即将提交到文件列表信息
- Repository:仓库区(或本地仓库)，就是安全存放数据的位置，这里有你提交到所有版本的数据。其中HEAD指向最新放入仓库的版本
- Remote:远程仓库，托管代码的服务器，可以简单的认为是你项目组中的一台电脑用于远程数据交换

---

git的工作流程一般是这样的:

1、在工作目录中添加、修改文件;	UserMapper.xml

2、将需要进行版本管理的文件放入暂存区域； git add

3、将暂存区域的文件提交到git仓库。 git commit  



因此，git管理的文件夹有三种状态：已修改(modified)	已暂存(staged)	已提交(committed)

```
git init 初始化项目
```



## **Git文件操作**

版本控制就是对文件的版本控制，要对文件进行修改、提交等操作，首先要知道文件当前在什么状态，不然可能会提交了现在还不想提交的文件，或者要提交的文件没提交上。

- Untracked:未跟踪，此文件在文件夹中，但并没有加入到git库，不参与版本控制。通过git add状态变为staged。
- Unmodify:文件已经入库，未修改，即版本库中的文件快照内容与文件夹中完全一致，这种类型的文件有两种去处，如果它被修改，而变为Modified。如果使用git rm移除版本库，则成为Untracked文件
- Modified：文件已修改，仅仅是修改，并没有进行其它操作。这个文件也有两个去处，通过git add可进入暂存staged状态，使用git checkout 则丢弃修改过，返回到unmodify状态，这个git checkout即从库中取出文件，覆盖当前修改！
- Staged：暂存状态。执行git commit 则将修改同步到库中，这时库中的文件和本地文件又变为一致，文件为Unmodify状态。执行git reset HEAD filename 取消暂存，文件状态为Modified。

上文说文件有四种状态，通过如下命令可以查看到文件的状态：

```bash
#查看指定文件状态
git status [filename]

#查看所有文件状态
git status

#添加所有文件到暂存区
git add . 

#提交暂存区中的内容到本地仓库 -m 提交的消息
git commit -m “消息内容”
```



## 文件忽略

**有些时候我们不想把某些文件纳入版本控制中，比如数据库文件，临时文件，设计文件等**

在主目录下建立“.gitignore”文件，此文件有如下规则：

1. 忽略文件中的空行或以（#）开始的行会被忽略
2. 可以使用Linux通配符。例如：（*）代表任意多个字符，问号（？）代表一个字符，方括号（[abc]）代表可选字符范围,大括号({a,s,d})代表可选字符串
3. 如果名称的最前面有一个感叹号(!)，表示例外规则，将不被忽略
4. 如果名称的最前面是一个路径分隔符(/)，表示要忽略的文件在此目录下，而子目录中的文件不忽略
5. 如果名称的最后面是一个路径分隔符(/)，表示要忽略的是此目录下该名称的子目录，而非文件（默认文件或目录都忽略）

```bash
#为注释
*.txt		#忽略所有 .txt结尾的文件
!lib.txt	#但lib.txt除外
/temp		#仅忽略项目根目录下的TODO文件，但不包括其它目录temp
build/		#忽略build/目录下的所有文件
doc/*.txt	#会忽略 doc/notes.txt 
```



## 查看远程库

**git remote -v：                      查看远程仓库详细信息，可以看到仓库名称**

**git remote remove orign：            删除orign仓库（如果把origin拼写成orign，删除错误名称仓库）**

**git remote add origin 仓库地址：       重新添加远程仓库地址**

**gti push -u origin master：            提交到远程仓库的master主干**