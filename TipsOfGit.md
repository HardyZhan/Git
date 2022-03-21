### GIT
#### 配置用户信息
* `git config --global user.name "HardyZhan"`
* `git config --global user.email "296566445@qq.com"`

#### 名词解释
* 工作区（Working Directory）：指的是在电脑里能看到的目录，比如mymenu文件夹就是一个工作区

* 版本库（Repository）：.git目录，Git的版本库里存了很多东西，其中最重要的就是称为stage（或者叫index）的暂存区，还有Git为我们自动创建的第一个分支master，以及指向master的一个指针叫HEAD。

#### 常用命令
* pwd 显示当前路径
* mkdir 创建文件夹
* git init 将当前目录变成git可以管理的仓库
* git add 添加文件到仓库
* git commit -m "a new file" 提交文件到仓库
<br> -m 后面输入的是本次提交的说明，提交成功后会显示：
<br> (1) file changed:*个文件被改动
<br> (2) insertions:插入了*行内容
<br> 注意：一次commit可以提交多个文件，所以可以多次add不同文件，一次提交。
* git log 查看历史记录
<br> 如果嫌输出信息太多，可以加上`--pretty=oneline`（一行显示）
<br> 其余参数 分支合并图(--graph)，提交校验码缩略(--abbrev-commit)
* git reset 回退历史版本
<br> `git reset --hard HEAD^`,HEAD^表示上一个版本，同理HEAD^^表示上上个版本，HEAD~100表示上一百个版本。
<br> `git reset --hard 1094adb7`也可以通过确切的版本号回退

* git reflog 查看历史命令，可以查看历史版本号
* git status 查看状态
* git diff HEAD -- test.txt 查看工作区和版本库里面最新版本的区别
* git checkout -- test.txt 撤销修改即丢掉工作区的修改，把test.txt文件在工作区的修改全部撤销
* git reset HEAD test.txt 把暂存区的修改撤销掉
* rm test.txt 工作区中删除文件，如果要删除版本库中的该文件，就用git rm
* git branch <name> 创建分支
* git checkout <name> 切换分支，加上参数-b表示创建并切换
* git branch 查看分支
* git merge <name> 合并某个分支到当前分支 `git merge dev`表示把dev分支的工作成果合并到master分支上
* git branch -d <name> 删除分支
* git remote 查看远程库的信息，加-v是查看详细信息
* git push origin master 将本底master分支推送到远程库
* git pull 抓取分支
