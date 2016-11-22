
## [Git服务器配置](http://weibo.com/GcsSloop)
## [官网教程](https://git-scm.com/book/zh/v2)

## Git常用命令

命令                            | 说明
--------------------------------|-----------------------------------------------------
git init				        | 使用当前目录作为 Git 仓库。git init [仓库名]，使用指定目录作为Git仓库。
git clone <repo> <directory>	| repo:Git 仓库。directory:本地目录。
git status		        | 查看在你上次提交之后是否有修改
git add "文件名"				          | git add 命令可将该文件添加到缓存
---------	| ---------------
git rm	"文件名"      | 从缓存区中移除
git mv "文件名" 	| 重命名文件 
---------	| ---------------
git branch		        | 列出分支
git branch [branchname]		        | 手动创建一个分支
git checkout [branchname]		        | 切换分支命令。当你切换分支的时候，Git 会用该分支的最后提交的快照替换你的工作目录的内容， 所以多个分支不需要多个目录。
git merge [branchname]		        | 合并分支到主分支。合并冲突就出现了，接下来我们需要手动去修改它。用 git add 告诉 Git 文件冲突已经解决
git branch -d [branchname]		        | 删除分支
---------	| ---------------
git remote		        | 查看当前配置有哪些远程仓库
git remote rm [alias]		        | 删除远程仓库
git fetch [alias]	        | 从远程仓库下载新分支与数据
git merge [alias]/[branch]		        | 将服务器上的任何更新合并到你的当前分支
git pull		        | 从远端仓库提取数据并尝试合并到当前分支，相当于 fetch 与 merge 操作
git commit	-m "第一次版本提交"	   |  将缓存区内容添加到仓库中，使用 -m 选项以在命令行中提供提交注释。
git push [alias] [branch]	        | 将你的 [branch] 分支推送成为 [alias] 远程仓库上的 [branch] 分支
---------	| ---------------
git log		        | 列出历史提交记录。用 --oneline 选项来查看历史记录的简洁的版本。用 --graph 选项，查看历史中什么时候出现了分支、合并。
