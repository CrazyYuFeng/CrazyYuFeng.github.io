ps： git add 进入 缓存区    git commit 进入 暂存区

git clone <http://××××>  <本地目录>  克隆项目到本地

git remote add <本地远程仓库名称> 远程仓库url

git remote -v 查看所有远程仓库分支

git remote rm <远程仓库分支名>  删除远程仓库分支

git fetch <远程仓库+分支>   下载代码到本地，保存本地更改代码

git branch 查看本地分支

git branch <本地分支名>  创建本地分支

git branch -D <本地分支名1 本地分支名2>   删除本地分支

git checkout <本地分支名>  切换分支

git checkout <本地分支名>  创建并且切换分支

git checkout --<文件名>  把工作区修改的文件撤销(不建议使用)

git status 查看当前git文件情况

git add <文件名> 添加文件到 暂存区

git commit -m'提交信息' 提交文件到暂存区

git pull <远程仓库+分支>  拉去远程代码到本地，合并本地更改代码

git push <远程仓库+分支>  推送代码到远程仓库(推送前git Pull)

git push -f <远程仓库+分支> 强制推送代码到远程仓库(本地代码落后于远端代码。 场景：git reset。 ps:不建议经常使用)

git diff <文件>  查看修改文件的差异

git clean -df   清除本地缓存(也就是还没有git add的文件)

git rm -rf <文件路径>   清楚缓存区文件（也就是git add之后的绿色文件）

git reset --hard <版本号>  回滚版本

git stash  备份工作区(场景: 切换分支时)

git stash apply 还原备份工作区

git remote prune origin 修剪，删除远程分支上本地不存在的分支(没怎么用过)

git push origin 远程分支 --delete   删除远程分支


