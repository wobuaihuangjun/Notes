# Git常用命令

命令                            | 说明
--------------------------------|-----------------------------------------------------
git init				        | 用 git init 在目录中创建新的 Git 仓库。
git clone git仓库路径		              | 拷贝一个 Git 仓库到本地
git status		        | 查看在你上次提交之后是否有修改
git add "文件名"				          | git add 命令可将该文件添加到缓存
git rm	"文件名"      | 从缓存区中移除
git mv "文件名" 	| 重命名文件 
git commit	-m "第一次版本提交"	   |  将缓存区内容添加到仓库中，使用 -m 选项以在命令行中提供提交注释。
git remote		        | 查看当前配置有哪些远程仓库
git fetch		        | 从远程仓库下载新分支与数据
git push [alias] [branch]	        | 将你的 [branch] 分支推送成为 [alias] 远程仓库上的 [branch] 分支
git pull		        | 从远端仓库提取数据并尝试合并到当前分支
