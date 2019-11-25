# 一 . 步骤

1. 在github 上创建一个issue, issue  一般来说是版本发布说明。比如本次更新了那些功能，修复了说明 bug 

2. 然后在 本地创建一个分支 branch ，或 直接在 github 上申请 merge request

   时会自动产生一个branch 。

3. 本地修改完代码后先查看git 状态 ：

     当前是在哪个项目分支下。

   git status

4. 如果不在想要的分支下 ，要切换分支

   git checkout newbranch

5. 添加修改的文件 或 目录到本地缓存区

   git add .    

    //      .   表示当前目录下全部文件

   //  git add 123 表示将123 这个文件加入缓存区 。

6. 可以对比一个当前文件与本地仓库已经保存的文件区别

   git diff

7. 可以查看一下当前的远程仓库

   git remote

8. 将缓存区中的修改文件或目录提交至本地仓库

   git commit -m "注释"

   // -m 后面添加的是描述， 即将描述此次提交的修改内容，便于自己或他人知道

9. 可以查看一下 commit 历史

   git log 

   //  查看最近3条提交记录

10. 如果最近提交记录太过频繁， 可以将多个 commit 合并

    git rebase -i HEAD~2

    // 将最近两次的commit 合并

    注意：如果在push 之前进行了rebase , 则 git push 命令后需要加上 --force

    即 ：git push --force origin branchname

11. 将本地仓库的文件上传到远程仓库指定的分支下

    git push origin 69-a-b-c

    // origin 是远程仓库默认的name

    // 69-a-b-c  是远程仓库的branch 的name 

12.  注意，如果如法push ， 可能是远程仓库有分支更新， 则需先从从远程仓库pull 或者采用fetch+merge来更新本地仓库，再重新commit并push

    git fetch       从远程获取最新到本地，不会自动merge 需要加上下面一行

    git merge origin/master

    或者 

    #  使用强制push的方法：

     git push -u origin master -f

    

    

    

    

    

    

    

    

    

    

    

    

    

    

    

    
    
    
    
    
    
    ​      









