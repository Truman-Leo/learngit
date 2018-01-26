# learngit


## install git in your PC

Download and install git-for-windows. Once you successfully install it, you will find "Git" -> 'Git bash' in the start menu. 

下载并安装git-for-windows安装程序。一旦安装成功，你可以在‘开始’菜单下看到‘Git’->'Git bash'启动选项。

## git usage guide

> if you plan to work from your github cloud repository, follow this.

### getting started - 1st time git configuration
```
# Your identity: set your user name and email addr.
git config --global user.name "[your name]"
git config --global user.email [your email addr]

# check your settings
git config --list
```

### clone repository from github online to your local disk
```
# clone a copy of an existing repository.
git clone https://github.com/trumanLuan/projectTrack
```

### record changes, and push the changes to local repository to cloud repository
```
# Just one note: if the repository doesn't exist in Github, first you will have to create it 
[click here](https://gist.github.com/c0ldlimit/4089101)
type NUL > README.md
git add README.md
git commit -m "my first commit"
git remote add origin https://github.com/c0ldlimit/vimcolors.git
git push -u origin master
```

### creat and manage repository using git commands locally

Lauch 'Git Bash' -> Creat new folder as your new repository corresponding to your new project -> init the folder to make it can be orangized by git command.

打开‘Git Bash’ -> 新建文件夹，你可以认为此文件夹为你的项目名称 -> 使用git init初始化文件夹，init命令把这个目录变成git可以管理的仓库。

```
mkdir learngit  # create a dir using shell/win cmd
git init # git envir initiation

type NUL > new.file # new a file using win cmd
touch new.file # new a file using linux cmd

git add new.file
git commit -m "add new.file"
```


## KEY git commands box

- git config 
- git init
- git add
- git commit  
- git status  
- git pull 
- git fetch
- git clone
- git push

The examples of these cmds are:

```
## [for what kind of usage]
git pull origin

## [for what kind of usage]
git clone git@github.com:[YourCount]/repositoryToBeCloned.git
```


## FAQ

### How to push multiple 'git commit'?

According to my practice, you need submit 'git add [The file changed]' -> 'git commit -m [The descrition]' -> git push. But, is that bothersome? why not git push once after multiple commit? Theoretically, once i add a file into git repository,the file should be ready for any git commands that work at the right time. However, I am requested to return the starting point from 'git add [the file to add]'. 

> maybe, I still don't understand how the git commands work underlying. Google it. (2016-11-03)

On the reason to this, I finally find a detailed explanation in a [git tutorial](https://git-scm.com/book/zh/v1/Git-%E5%9F%BA%E7%A1%80-%E8%AE%B0%E5%BD%95%E6%AF%8F%E6%AC%A1%E6%9B%B4%E6%96%B0%E5%88%B0%E4%BB%93%E5%BA%93) (Chinese webpages).
究其原因，"...实际上 Git 只不过暂存了你运行 git add 命令时的版本，如果现在提交，那么提交的是添加注释前的版本，而非当前工作目录中的版本。所以，运行了 git add 之后又作了修订的文件，需要重新运行 git add 把最新版本重新暂存起来..."

### fatal: refuse to merge unrelated histories.

According to my practice, git rm the file, and git clone remote repository as local again.
I tried to git rm the file, and git init again -> git pull, and I failed to make the origin and master the same line.

### how to add a folder in git repository?

git doesn't store empty folders. Just make sure there's a file in the folder like *doc/foo.txt* and run git add doc or *git add doc/foo.txt* and the folder will be added to your local repo once you've committed (and appear on github once you've pushed it).

### how to delete files, or folders in your local repository?

> git rm fileToBeRemoved


### any more?
