# Git学习指南

## 1.Git安装  

1. 进入[git官网](https://git-scm.com/downloads)下载相应版本.  
2. 打开应用程序安装,除了安装路径一路默认到最后就行了.  
3. 打开Git Bash 输入git 看到一大堆输出 证明安装完成  
```
usage: git [--version] [--help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           [--super-prefix=<path>] [--config-env=<name>=<envvar>]
           <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone     Clone a repository into a new directory
   init      Create an empty Git repository or reinitialize an existing one

.....

collaborate (see also: git help workflows)
   fetch     Download objects and refs from another repository
   pull      Fetch from and integrate with another repository or a local branch
   push      Update remote refs along with associated objects

'git help -a' and 'git help -g' list available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.
See 'git help git' for an overview of the system.

```


## 2.Git使用

接下来的操作是按照创建一个新的git项目来操作的  
以下所有操作均在Git Bash下进行
#### 1. 创建git仓库  
1. **mkdir**并**cd** 文件夹(此文件夹之后将做为git仓库)
2. **git status** 查看仓库状态
    ```
    fatal: not a git repository (or any of the parent directories): .git  
    这样就表明这个文件夹还不是git仓库
    ```
3. **git init**  将当前文件夹初始化为git仓库,在git仓库下的所有文件才会被git所管理
    ```
    Initialized empty Git repository in E:/Kyrios/code/hello_code/.git/  
    创建了一个.git文件 证明git仓库初始化成功
    ```
    现在再执行git status 会发现hello_code目录已经成为一个git仓库了，并且默认进入git仓库的master分支，即主分支。在这里，我们需要注意的是Untracked fies提示，它表示hello_code仓库中有文件没有被追踪，并提示了具体没有被追踪的文件为MarkDown学习指南.md，还提示了我们可以使用git add命令操作这个文件. 
    ```
    $ git status
        On branch master
        No commits yet
        Untracked files:
            (use "git add <file>..." to include in what will be committed)
                "MarkDown\345\255\246\344\271\240\346\214\207\345\215\227.md"
    nothing added to commit but untracked files present (use "git add" to track)
    ```
#### 2. 创建身份识别  
**git config user.email "354034186@qq.com"**  
**git config user.name "Kyrios"**  

    有时候会提示你没有认真身份,也就是需要你登录一下，确认你的身份，但是不要按照其提示输入，
    先输入命令git config user.name “username”，换行输入git config user.email “email”
    输入正确的之后就能使用 git add 、commit等命令进行版本控制了
    
    
#### 3. 将一个或多个文件添加到暂存区(跟踪一个或多个文件)  
**git add**  

    $ git add MarkDown学习指南.md

    如果什么都没有那就证明添加成功了,如果报错了注意文件后面是不是加空格了
    
#### 4. 将暂存区的改动提交,git会永久保存这次提交  
**git commit -m"提交信息"**  
    
    $ git commit -m "将markdown文档提交git监管"
    [master (root-commit) 5fd5223] 将markdown文档提交git监管
    1 file changed, 355 insertions(+)
    create mode 100644 "MarkDown\345\255\246\344\271\240\346\214\207\345\215\227.md"
    这样就表示提交成功了
    
#### 5. 查看git操作日志  
1. **git log**  
    此命令能查看详细的版本号 用于回退
    ```
    $ git log
    commit 5fd5223cf5596ef8c2a24f683635e0852e4fa738 (HEAD -> master)
    Author: Kyrios <354034186@qq.com>
    Date:   Thu Dec 9 11:01:49 2021 +0800

    将markdown文档提交git监管
    ```
2. **git reflog**   
    此命令只能看到log列表
    ```
    $ git reflog
    5fd5223 (HEAD -> master) HEAD@{0}: commit (initial): 将markdown文档提交git监管
    ```

#### 6. 操作分支
1. **git branch**  
    查看所有分支 
    ```
    $ git branch
    d2v
    * dev
    master
    ```
2. **git branch d2v**  
    创建一个名为d2v的分支,这样创建分支并不会跳转到新创建的分支
    ```
    kyrio@DESKTOP-S9RF950 MINGW64 /e/Kyrios/code/hello_code (dev)
    $ git branch d2v

    kyrio@DESKTOP-S9RF950 MINGW64 /e/Kyrios/code/hello_code (dev)

    ```
3. **git checkout -b 分支名**   
    创建一个名为dev的分支 并跳转到dev   
    ```
    $ git checkout -b dev
    Switched to a new branch 'dev'
    kyrio@DESKTOP-S9RF950 MINGW64 /e/Kyrios/code/hello_code (dev)
    ```
4. **git checkout master**    
    切换到msater分支
    ```
    kyrio@DESKTOP-S9RF950 MINGW64 /e/Kyrios/code/hello_code (dev)
    $ git checkout master
    Switched to branch 'master'
    kyrio@DESKTOP-S9RF950 MINGW64 /e/Kyrios/code/hello_code (master)
    ```
5. **git branch -d d2v**  
    正常删除d2v分支,确保分支已合并到主分支
    ```
    kyrio@DESKTOP-S9RF950 MINGW64 /e/Kyrios/code/hello_code (master)
    $ git branch -d d2v
    Deleted branch d2v (was 5fd5223).
    ```
6. **git branch -D dev**  
    强制删除dev分支
    ```
    kyrio@DESKTOP-S9RF950 MINGW64 /e/Kyrios/code/hello_code (master)
    $ git branch -D dev
    Deleted branch dev (was 5fd5223).
    ```
7. **git merge tag**  
    将tag分支合并到当前分支
    ```
    kyrio@DESKTOP-S9RF950 MINGW64 /e/Kyrios/code/hello_code (master)
    $ git merge tag
    Already up to date.
    ```
## 3.远程相关操作   
将git和github关联有两种方式
1. **本地原有代码直接本地建仓库 关联到github监管**
    1. 本地仓库关联远程仓库   
        **git remote add origin `https://github.com/Kyrios0626/HelloCode.git`**   
        为本地仓库绑定远程仓库地址,远程仓库名为origin 
        ```
        $ git remote add origin https://github.com/Kyrios0626/HelloCode.git

        kyrio@DESKTOP-S9RF950 MINGW64 /E/Kyrios/code/hello_code (master)
        ```   
        *origin* 表示你自己给远程仓库起了个本地识别的名字,  
        以后git识别到origin就表示它是远程的hellow code仓库  
    
    2. 提交本地代码到远程仓库  
        **git push -u origin master**  
        将本地 ***当前*** 分支与远程 ***master*** 分支进行绑定,并推送代码  
        绑定之后,下次如果在推本地分支,可以直接使用git push 命令.  
        ```
        $ git push -u origin master
        Enumerating objects: 3, done.
        Counting objects: 100% (3/3), done.
        Delta compression using up to 8 threads
        Compressing objects: 100% (3/3), done.
        Writing objects: 100% (3/3), 4.24 KiB | 2.12 MiB/s, done.
        Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
        remote:
        remote: Create a pull request for 'master' on GitHub by visiting:
        remote:      https://github.com/Kyrios0626/HelloCode/pull/new/master
        remote:
        To https://github.com/Kyrios0626/HelloCode.git
         * [new branch]      master -> master
        Branch 'master' set up to track remote branch 'master' from 'origin'.
        ```
    
    *master* 代表你要提交的远程分支的名字  
    没有分支会自动创建分支
2. 本地没有代码,直接将远程代码克隆下来

    
    
 
    





git push -u origin 远程分支   
将本地分支与远程分支进行绑定,并推送代码,绑定之后,下次如果在推本地分支,可以直接使用git push 命令.  
git clone 远程仓库地址  克隆一个项目  
git pull origin 远程分支  拉取远程仓库对应分支的变化代码  

git reset --hard 1162897 版本回退  

# tag标签
    
    tag是git版本库的一个标记，指向某个commit的指针。
    tag主要用于发布版本的管理，一个版本发布之后，我们可以为git打上 v.1.0.1 v.1.0.2 ...这样的标签。

    tag感觉跟branch有点相似，但是本质上和分工上是不同的：

    tag 对应某次commit, 是一个点，是不可移动的。
    branch 对应一系列commit，是很多点连成的一根线，有一个HEAD 指针，是可以依靠 HEAD 指针移动的。
    
    所以，两者的区别决定了使用方式，改动代码用 branch ,不改动只查看用 tag。
    tag 和 branch 的相互配合使用，有时候起到非常方便的效果，
    例如：已经发布了 v1.0 v2.0 v3.0 三个版本，
    这个时候，我突然想不改现有代码的前提下，在 v2.0 的基础上加个新功能，作为 v4.0 发布。
    就可以检出 v2.0 的代码作为一个 branch ，然后作为开发分支。
    
1. **git tag v1.0**  
    创建一个名为v1.0的标签
2. **git tag**  
    查看所有标签
3. **git push origin v1.0**   
    将v1.0标签推送到远程仓库   
4. **git push origin --tags**  
    将所有本地标签一次全部推送到远程
5. **git ls-remote --tags origin**  
    查看所有远程标签
6. **git tag -d v1.0**  
    删除本地名为v1.0的标签

    