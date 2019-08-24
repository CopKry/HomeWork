让我的本地git仓库和github仓库建立联系
第一步 创建ssh key  
ssh-keygen -t rsa -C "yyx219@qq.com"

关联远程仓库
git remote add origin git@github.com:yyx219/38du.git

第一次向远程仓库推送数据
git push -u origin master

第二次可简化成
git push
有了第一个属于自己的远程仓库

从远程仓库克隆一个仓库到本地
git clone git@github.com:yyx219/38du.git




在远程创建分支并推送
git push --set-upstream origin dev

查看分支
git branch 
创建分支
git branch name
切换分支
git checkout name
创建分支 并切换到分支
git checkout -b dev  
合并分支
git merge dev
删除分支
git branch -d name

手动解决合并冲突。人工选择需要留下的代码
再重新
git add .
git commit 
git push

查看分支合并情况
git log --graph --pretty=oneline --abbrev-commit
查看分支合并图
git log --graph


表示禁用 fast forward 模式
$ git merge --no-ff -m "merge no-ff" dev

git stash  
git stash  list

master  主分支  时刻需要同步
dev 开发分支。所有团队成员都在这上面干活。所以要推送
bug 分支 没有必要推送
new 看情况

创建远程分支origin/dev 到本地 
 git checkout -b dev origin/dev


多人工作
可以用 git push dev 推荐修改
如果失败，先用 git pull 远程合并到我本地
如果合并冲突。解决冲突。再提交

git branch -v 查看远程库分支