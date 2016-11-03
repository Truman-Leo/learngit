# learngit

## Content
- 在本地PC上安装git（Windowns）
- creat repository in local PC
- add remote repository 
- Git commands
- ...

## install git in your PC

Download and install git-for-windows. Once you successfully install it, you will find "Git" -> 'Git bash' in the start menu. 

下载并安装git-for-windows安装程序。一旦安装成功，你可以在‘开始’菜单下看到‘Git’->'Git bash'启动选项。

## creat repository in local PC

Lauch 'Git Bash' -> Creat new folder as your new repository corresponding to your new project -> init the folder to make it can be orangized by git command.

打开‘Git Bash’ -> 新建文件夹，你可以认为此文件夹为你的项目名称 -> 使用git init初始化文件夹，init命令把这个目录变成git可以管理的仓库。

> mkdir learngit

> ls -a

> git init

> ls -a


## Git commands

### git init

See previous section.

参考前述。

### git add

Creat new file under the folder, the file contains your text or codes. That depends on you -> add the file to git repository.

在文件夹下新建文件，文件可以包含你的博客、代码等，内容根据你的需要而定 -> 将此文件添加到git仓库。

> cd [newFolder]

> **git add** [new.file] 

### git commit

Once you update your text or code, you need commit the changes to corresponding git repository. 

> **git commit** -m "Your description text/your note on this changes"

简单解释一下git commit命令，-m后面输入的是本次提交的说明，可以输入任意内容。

### git status

check current status of local git repository.

### git pull

pull the changes in the remote repository to local repository. synchronize the local folder with the remove one. The usage is:
>git pull origin

### git fetch

### git clone

### git add

## FAQ

### How to push multiple 'git commit'? 

According to my practice, you need submit 'git add [The file changed]' -> 'git commit -m [The descrition]' -> git push. But, is that bothersome? why not git push once after multiple commit? Theoretically, once i add a file into git repository,the file should be ready for any git commands that work at the right time. However, I am requested to return the starting point from 'git add [the file to add]'. 

> maybe, I still don't understand how the git commands work underlying. Google it. (2016-11-03)
