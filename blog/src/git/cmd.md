## git 常用命令

#### git init
git init 初始化一个仓库
```
cmd:
    git init <repo>
    git init --bare <repo>
exp:
    // 创建一个空的目录
    mkdir target
    // 进入这个空目录
    cd target
    // 执行初始化命令
    git init
or
    // 执行初始化命令 初始化一个裸库,不可以执行一般的git命令
    git init --bare
```
[git init 命令说明](https://moelove.info/2016/12/04/Git-%E6%9C%AC%E5%9C%B0%E4%BB%93%E5%BA%93%E5%92%8C%E8%A3%B8%E4%BB%93%E5%BA%93/)  
.git目录下的配置
```
...
git init
...
[core]
	repositoryformatversion = 0
	filemode = false
	bare = false
	logallrefupdates = true
	symlinks = false
	ignorecase = true
    ...
git init  --bare
...
[core]
	repositoryformatversion = 0
	filemode = false
	bare = true
	ignorecase = true
	precomposeunicode = true
```

#### git clone 
```
// 克隆仓库
git clone <route adress>

// 克隆指定分支的仓库
git clone -b <branch name> <route adress>
```

#### git status  
1 git status 命令用于显示工作目录和暂存区的状态。  
2 git status 不显示已经commit到项目历史中去的信息。看项目历史的信息要使用 git log。
```
cmd:
    git status [<options>…​] [--] [<pathspec>…​]
exp:
    # On branch master
    # Changes to be committed:  (已经在stage区, 等待添加到HEAD中的文件)
    # (use "git reset HEAD <file>..." to unstage)
    #
    #modified: hello.py
    #
    # Changes not staged for commit: (有修改, 但是没有被添加到stage区的文件)
    # (use "git add <file>..." to update what will be committed)
    # (use "git checkout -- <file>..." to discard changes in working directory)
    #
    #modified: main.py
    #
    # Untracked files:(没有tracked过的文件, 即从没有add过的文件)
    # (use "git add <file>..." to include in what will be committed)
```

#### git log
```
// 查看提交历史
// 默认输出 commit hash, author, date, commit message
/**
exp:
commit 8c0d740b0afcb1ff47b2693c33914ced9a42e966 (HEAD -> master, origin/master, origin/HEAD)
Author: Mattle <coin1994@outlook.com>
Date:   Tue Nov 12 22:58:36 2019 +0800

    handler commit
**/
git log

// 简化 git log 输出
git log --oneline

// --stat 是在 git log 的基础上输出文件增删改的统计数据
git log --stat

// 控制输出每个commit 具体的修改内容 以diff的形式给出
git log -p

// 限定git log 输出
git log -n 
exp:
git log -2
...
```
#### git add 
```
// 不加参数默认为将修改操作的文件和未跟踪新添加的文件添加到git系统的暂存区，注意不包括删除
git add  . 
//表示将所有的已跟踪的文件的修改与删除和新增的未跟踪的文件都添加到暂存区。
git add --all / git add -A

//表示将已跟踪文件中的修改和删除的文件添加到暂存区，不包括新增加的文件，注意这些被删除的文件被加入到暂存区再被提交并推送到服务器的版本库之后这个文件就会从git系统中消失了。
git add --update / git add -u 
...
以上三个命令已经足够日常使用了
...

// 这个命令它也是作用于版本库中已被跟踪的文件中的执行过修改与删除操作的文件。
git add -i

```
#### git commit 

#### git push

#### git pull

#### git checkout

#### git branch

#### git mearge

#### git rebase

#### git stash





