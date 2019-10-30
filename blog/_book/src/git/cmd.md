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

#### git add 

#### git commit 

#### git push

#### git pull

#### git checkout

#### git branch

#### git mearge

#### git rebase

#### git stash





