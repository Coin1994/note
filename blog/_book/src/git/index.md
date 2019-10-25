## GIT 环境搭建  
##### 1. windows 下 git 环境搭建  
下载 [Git For Windows](https://git-scm.com/downloads/)正常安装 windows 程序
##### 2. linux 下 git 环境搭建


## GIT 全局配置
```
// 全局配置
git config --global user.name "Your Name"
git config --global user.email "email@example.com"

// 查看配置
// 系统配置
git config --system  --list
// 当前用户配置
git config --global  --list
// 当前仓库配置信息
git config --local  --list
```

## GIT 多账户配置
```
// 第一步
ssh-keygen -t rsa -C "xxx@qq.com"
#设置文件名，自动生成私钥和公钥(.pub)
Enter file in which to save the key (/c/Users/icecr/.ssh/id_rsa): id_github_rsa

// 第二步
#在ssh目录下新建config文件
# gitee
Host gitee.com
HostName gitee.com
PreferredAuthentications publickey
IdentityFile /c/Users/coin1/.ssh/id_gitee_rsa

# github
Host github.com
HostName github.com
PreferredAuthentications publickey
IdentityFile /c/Users/coin1/.ssh/id_github_rsa

// 第三步
设置git公匙

// 第四步
 ssh -T git@gitee.com
 ssh -T git@github.com
```
  


