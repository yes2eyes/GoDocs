# Git 教程


- 安装
- 初始化
- 本地提交
- 远程推送
- 分支切换、管理、合并、删除、查看
- 内容回滚
- 删除内容
- .gitignore
- .git/info/exclude




- git 客户端的使用

```

usage: git [--version] [--help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p | --paginate | -P | --no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           <command> [<args>]

These are common Git commands used in various situations:

start a working area (see also: git help tutorial)
   clone      Clone a repository into a new directory
   init       Create an empty Git repository or reinitialize an existing one

work on the current change (see also: git help everyday)
   add        Add file contents to the index
   mv         Move or rename a file, a directory, or a symlink
   reset      Reset current HEAD to the specified state
   rm         Remove files from the working tree and from the index

examine the history and state (see also: git help revisions)
   bisect     Use binary search to find the commit that introduced a bug
   grep       Print lines matching a pattern
   log        Show commit logs
   show       Show various types of objects
   status     Show the working tree status

grow, mark and tweak your common history
   branch     List, create, or delete branches
   checkout   Switch branches or restore working tree files
   commit     Record changes to the repository
   diff       Show changes between commits, commit and working tree, etc
   merge      Join two or more development histories together
   rebase     Reapply commits on top of another base tip
   tag        Create, list, delete or verify a tag object signed with GPG

collaborate (see also: git help workflows)
   fetch      Download objects and refs from another repository
   pull       Fetch from and integrate with another repository or a local branch
   push       Update remote refs along with associated objects

'git help -a' and 'git help -g' list available subcommands and some
concept guides. See 'git help <command>' or 'git help <concept>'
to read about a specific subcommand or concept.

```


## Github 使用

- 秘钥设置
- 介绍：账户、仓库、信息


## Git 和 Github


## 设置

```

git config --local user.email "wuxiaoshen@shu.edu.cn"
git config --global user.email "wuxiaoshen@shu.edu.cn"

git config --local --list

```


## 命令集合

- git blame <file>
- git commit --amend
- git checkout remotes/origin/nsy-region-1128
- git branch -m old new
- git config --local user.email "wuxiaoshen@shu.edu.cn"
- git log -p -2


## Git commit message

```
feat：新功能（feature）
fix：修补bug
docs：文档（documentation）
style： 格式（不影响代码运行的变动）
refactor：重构（即不是新增功能，也不是修改bug的代码变动）
test：增加测试
chore：构建过程或辅助工具的变动
```

:bowtie:

:grinning:

:books:

## Git 如何忽略本地的文件

- .gitignore
- .git/info/exclude  + git update-index --assume-unchanged [file]
- git update-index --skip-worktree [file]

## 如何给 github 添加 tag

``` 
git tag -a v1.0 -m "comment" //  创建 tag 并添加备注
git push origin v1.0 // 推送 tag 到远端分支
git push origin --delete tag v1.1.8beta0

```


## 如何给开源项目提 Pull Request

- fork 开源项目
- git clone fork 之后的开源项目
- 修改项目代码
- git add .
- git commit -m "message"
- git push
- web 端：Pull Request
- 填写 Issue 

## 克隆单个文件或者文件夹

- git init filepath && cd filepath // 初始化
- git config core.sparsecheckout true // 允许克隆子目录
- echo '文件或者文件夹' >> .git/info/sparse-checkout // 设置需要下载的文件或者文件夹
- git remote add origin git@address // 关联远程地址
- git pull origin master // 下载


## Git 工作流

## 项目迁移


```
.git/config
remote "origin"
   url = 新项目地址

执行：git push -u origin master
```