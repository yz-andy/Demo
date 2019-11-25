## Git 学习笔记 

##### 2019-11月-8日

* 打开终端窗口

*  查看主题目录  ls    cd ..

* git status  查看git 状态   

*  yz@yz-ThinkPad-T420:~/test$ git status
  位于分支 master
  无文件要提交，干净的工作区

* touch a     触摸    a 文件 

* git status    

*  yz@yz-ThinkPad-T420:~/test$ git status
  位于分支 master
  未跟踪的文件:
    （使用 "git add <文件>..." 以包含要提交的内容）

  	a

  提交为空，但是存在尚未跟踪的文件（使用 "git add" 建立跟踪）

* git commit -m "提交第一次"

    yz@yz-ThinkPad-T420:~/test$ git commit -m "提交第一次"
	​		[master eeecb04] 提交第一次
	 		1 file changed, 0 insertions(+), 0 deletions(-)
	 		create mode 100644 agit remote add origin https://github.com/yz-andy/yzandy.git

回车 ：用户名  回车后 ‵继续     password 

 git push -u origin master 回车后 窗口显示：

Username for 'https://github.com': yz-andy           
Password for 'https://yz-andy@github.com': 
对象计数中: 3, 完成.
写入对象中: 100% (3/3), 218 bytes | 218.00 KiB/s, 完成.
Total 3 (delta 0), reused 0 (delta 0)
To https://github.com/yz-andy/yzandy.git

 * [new branch]      master -> master
分支 'master' 设置为跟踪来自 'origin' 的远程分支 'master'。



《《其中途出现异常无法正常连接远程仓库》》

克隆/ 暂存/ 提交/ 拉取/抓取/推送
克隆远程仓库到本地： git clone 远程地址

查看未暂存文件修改情况： git diff
查看暂存区的文件修改内容： git diff --cached 或 git diff --staged
暂存文件：git add 文件路径 或 git add .
撤销未暂存文件的修改：git checkout -- 文件名（操作不可逆）
恢复删除的文件：step1: git reset HEAD 文件名 撤销删除文件的暂存 step2: git checkout -- 文件名 将删除的文件进行恢复
取消文件暂存： git reset HEAD 文件名
查看commit日志：git log 或 git log -3（显示3条）
查看简约日志：git log --oneline -3（只显示commit-hash 和 commit info）
查看最近一次提交的差异： git log -p -1
查看所有差异： git log -p

提交暂存：git commit
暂存文件并提交： git commit -a
添加描述提交：git commit -m "内容描述"
暂存添加描述提交： git commit -a -m "内容描述"

拉取远端：git pull

抓取分支：git fetch origin 分支名
抓取远端所有分支：git fetch

推送至远端：git push origin 分支名
跟踪远端分支：git push -u origin 分支名
查看远端仓库地址： git remote -v

操作 branch
查看状态：git status

查看简写状态： git status -s 

(M 修改， A 添加， D 删除， R 重命名， ?? 未追踪)

查看分支：git branch

查看所有分支最后一次提交：git branch -v

创建分支：git branch 分支名

检出分支：git checkout 分支名

创建 + 检出分支：git checkout -b 分支名

合并某分支到当前分支：git merge 分支名

合并某分支到当前分支并添加注释信息：git merge 分支名 --no-ff -m "内容描述"

删除分支：git branch -d 分支名

查看远程分支：git branch -a

删除远程分支：git push origin --delete 分支名 或 git push origin :分支名

操作 tag

显示所有标签： git tag

创建标签： git tag -a 标签名 -m “标签描述”

删除本地标签：git tag -d 标签名

显示标签描述： git show 标签名

给之前的commit 创建tag： git tag -a 标签名 -m “标签描述” 

commit-hash
将标签推送到远端：git push origin 标签名

推送所有标签： git push origin --tags

删除远程标签：git push origin -d 标签名 或 git push origin --delete tag 标签名

合并 （merge）/变基(衍合)（rebase） / 摘樱桃（cherry-pick）
三个操作都是分支间的操作， 每项操作都有可能得到代码冲突，遇到冲突的情况一定要先解决掉冲突才可以commit、push到远端。

合并分支： git merge 分支名

 （合并分支会在原来的基础上新增一个commit，提交log是按时间排序）

变基分支: git rebase 分支名 （变基分支不会新增一个commit , 提交log是按两个分支的提交记录续接下去的）

摘取一个commit：git cherry-pick 其他分支的commit-hash 

(相当于直接把别的分支的某些提交直接摘到当前分支)
摘取多个commit：git cherry-pick commit-hash1..commit-hash2（1到2之间的commits，不包括1）或 git cherry-pick commit-hash1^..commit-hash2（1到2之间的commits，包括1）