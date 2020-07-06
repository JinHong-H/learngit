# Git笔记

## Git基础操作

### cd

+ cd : change directory的简写，改变目录的意思，就是切换到哪个目录下， 如 cd e:\fff  切换 E 盘下面的fff 目录。当我们用cd 进入文件夹时,我们可以使用 通配符*, cd f*,  如果E盘下只有一个f开头的文件夹,它就会进入到这个文件夹.

+ cd .. 回退到上一个目录。我们在写js，引入文件时，.. 表示的就是上一个目录, 所以 cd .. 回退到上一个目录就很好理解了。注意，cd 和两个点点..之间有一个空格,  

### pwd

+ pwd : print working directory, 打印工作目录，它会显示我们当前所在的目录路径。

### ls

+ ls: list, 列出当前目录中的所有文件，     只不过ll(两个ll)列出的内容更为详细。

### touch

+ touch : 新建一个文件 如 touch index.js 就会在当前目录下新建一个index.js文件。

### rm

+ rm:  remove，删除一个文件, rm index.js 就会把index.js文件删除.

### mkdir

+ mkdir: make directory 新建一个目录,就是新建一个文件夹. 如mkdir src 新建src 文件夹.

### rm -r

+ rm -r :  删除一个文件夹， r (recusive 是递归的意思)， 删除用的就是递归，先删除文件夹里面的内容，再删除文件夹。 rm -r src 删除src目录。

### mv

+ mv 移动文件, mv index.html src   index.html 是我们要移动的文件, src 是目标文件夹,当然, 这样写,必须保证文件和目标文件夹在同一目录下.

### reset

+ reset 清屏，把git bash命令窗口中的所有内容清空。

## Git创建仓库

### git init

+ Git 使用 git init 命令来初始化一个 Git 仓库，Git 的很多命令都需要在 Git 的仓库中运行，所以 git init 是使用 Git 的第一个命令。

### git add <文件名>(后缀)

+ 将文件加入仓库
  
### git commit -m "备注信息(干了什么)"

+ 将文件提交到仓库

## 注意区分工作区和缓存区

## 版本回退

+ HEAD指向的版本就是当前版本，因此，Git允许我们在版本的历史之间穿梭，使用命令```git reset --hard commit_id```。

+ 穿梭前，用```git log```可以查看提交历史，以便确定要回退到哪个版本。

+ 要重返未来，用```git reflog```查看命令历史，以便确定要回到未来的哪个版本。

## 撤销修改

+ 场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令```git checkout -- file```(让这个文件回到最近一次```git commit```或```git add``时的状态)。

+ 场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令```git reset HEAD <file>```，就回到了场景1，第二步按场景1操作。

+ 场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交，参考版本回退一节，不过前提是没有推送到远程库。

## 删除文件

+ rm <文件名>(后缀) 删除文件，与直接找到文件并删除效果相当

+ 要在版本库中删除该文件，应该用```git rm```删掉，并且```git commit -m "备注消息"```

+ 若误删文件，但版本库中仍然有可以用```git checkout -- <文件名>(后缀)```将误删的文件恢复到最新版本

## 添加远程库

+ 要关联一个远程库，使用命令```git remote add origin git@server-name(github用户名):path/repo-name.git(仓库名)```；

+ 关联后，使用命令```git push -u origin master``` ***第一次*** 推送master分支的所有内容；

+ ***此后，每次本地提交后，只要有必要，就可以使用命令```git push origin master```推送最新修改***；

+ 远程分支同步的时候，如果是同步当前分支，直接用``` git push ```指令即可，如果不是默认分支，则需要指明分支名称
如：```git push origin dev(分支名)```

## 从远程库克隆

+ 要克隆一个仓库，首先必须知道仓库的地址，然后使用git clone命令克隆。示例：
  
```(Git)
git clone git@github.com:LHLHJH/gitskills.git
```

+ Git支持多种协议，包括https，但ssh协议速度最快

## 创建与合并分支

+ 查看分支：```git branch```

+ 创建分支：```git branch <name>```

+ 切换分支：```git checkout <name>```或者```git switch <name>```

+ 创建+切换分支：```git checkout -b <name>```或者```git switch -c <name>```

+ 合并某分支到当前分支：```git merge <name>(需要合并过来的分支名)```，合并分支之后可以将原来的分支删除

+ 删除分支：```git branch -d <name>```

## 解决冲突

+ 当Git无法自动合并分支时，就必须首先解决冲突。解决冲突后，再提交，合并完成。解决冲突就是把Git合并失败的文件手动编辑为我们希望的内容，再提交。用git log --graph命令可以看到分支合并图

## 分支策略管理

+ 在实际开发中，我们应该按照几个基本原则进行分支管理：

   1. 首先，master分支应该是非常稳定的，也就是仅用来发布新版本，平时不能在上面干活；

   2. 那在哪干活呢？干活都在dev分支上，也就是说，dev分支是不稳定的，到某个时候，比如1.0版本发布时，再把dev分支合并到master上，在master分支发布1.0版本；

   3. 你和你的小伙伴们每个人都在dev分支上干活，每个人都有自己的分支，时不时地往dev分支上合并就可以了。

+ Git分支十分强大，在团队开发中应该充分应用。

+ 合并分支时，加上--no-ff参数就可以用普通模式合并，合并后的历史有分支，能看出来曾经做过合并，而fast forward合并就看不出来曾经做过合并。示例如下：
  
```(git)
git merge --no-ff -m "merge with no-ff" dev(分支名)
```

+ 注意 “-m”参数的使用，主要是用来记录操作的信息，便于后期查看都进行了什么操作，在这里的信息一定要直观，简单，明了

## Bug分支

+ 修复bug时，我们会通过创建新的bug分支进行修复，然后合并，最后删除；

+ 当手头工作没有完成时，先把工作现场```git stash```一下(可以把当前工作现场“储藏”起来，等以后恢复现场后继续工作)，然后去修复bug，修复后，再```git stash pop```，回到工作现场；

+ 用```git stash list```命令可以查看刚才的工作现场，工作现场还在，Git把stash内容存在某个地方了，但是需要恢复一下，有两个办法：

   1. 一是用git stash apply恢复，但是恢复后，stash内容并不删除，你需要用git stash drop来删除；

   2. 另一种方式是用git stash pop，恢复的同时把stash内容也删了：

+ 在master分支上修复的bug，想要合并到当前dev分支，可以用```git cherry-pick <commit>```命令，把bug提交的修改“复制”到当前分支，避免重复劳动。

## Feature分支

+ 开发一个新feature，最好新建一个分支；
  
+ 如果要丢弃一个没有被合并过的分支，可以通过```git branch -D <name>```强行删除。

## 多人协作

### 一些基本原则

+ master分支是主分支，因此要时刻与远程同步；

+ dev分支是开发分支，团队所有成员都需要在上面工作，所以也需要与远程同步；

+ bug分支只用于在本地修复bug，就没必要推到远程了，除非老板要看看你每周到底修复了几个bug；

+ feature分支是否推到远程，取决于你是否和你的小伙伴合作在上面开发。

### 多人协作工作模式

+ 首先，可以试图用```git push origin <branch-name>```推送自己的修改；

+ 如果推送失败，则因为远程分支比你的本地更新，需要先用```git pull```试图合并；

+ 如果合并有冲突，则解决冲突，并在本地提交；

+ 没有冲突或者解决掉冲突后，再用```git push origin <branch-name>```推送就能成功！

+ 如果```git pull```提示```no tracking information```，则说明本地分支和远程分支的链接关系没有创建，用命令```git branch --set-upstream-to <branch-name> origin/<branch-name>```。

### 操作归纳

+ 查看远程库信息，使用```git remote -v```；

+ 本地新建的分支如果不推送到远程，对其他人就是不可见的；

+ 从本地推送分支，使用```git push origin branch-name```，如果推送失败，先用```git pull```抓取远程的新提交；

+ 在本地创建和远程分支对应的分支，使用```git checkout -b branch-name origin/branch-name```，本地和远程分支的名称最好一致；

+ 建立本地分支和远程分支的关联，使用```git branch --set-upstream branch-name origin/branch-name```；

+ 从远程抓取分支，使用```git pull```，如果有冲突，要先处理冲突。

## Rebase

+ rebase操作可以把本地未push的分叉提交历史整理成直线；

+ rebase的目的是使得我们在查看历史提交的变化时更容易，因为分叉的提交需要三方对比。

## 标签操作

### 创建与查看

+ 命令```git tag <tagname>```用于新建一个标签，默认为HEAD(即最新的commit)，也可以指定一个commit id；

+ 命令```git tag -a <tagname> -m "blablabla..."```可以指定标签信息；

+ 命令```git tag```可以查看所有标签。

+ 标签不是按时间顺序列出，而是按字母排序的。可以用```git show <tagname>```查看标签信息(包括参数 -m"XXX"中的信息)

### 删除与同步

+ 命令```git push origin <tagname>```可以推送一个本地标签；

+ 命令```git push origin --tags```可以推送全部未推送过的本地标签；

+ 命令```git tag -d <tagname>```可以删除一个本地标签；

+ 命令```git push origin :refs/tags/<tagname>```可以删除一个远程标签。

![RUNOOB 图标](https://img-blog.csdnimg.cn/20200311181420510.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L2FhODA0NzM4NTM0,size_16,color_FFFFFF,t_70)
