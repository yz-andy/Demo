```csharp
# 进入要使用Git的目录
cd gitUse
# 初始化一个git仓库
git init
# 项目中应该有你编辑的文件等等，将他们从工作区放到缓存区，也就是SourceTree中的 “暂存”
git add .
# 提交到本地仓库，并填写本次提交的描述信息
git commit -m "这里是本次提交的描述信息"
# 新建远端的仓库，去对应的git网站新建就好了
https://github.com/yylittlecat/gitUse.git
# 关联本地与远程的仓库
git remote add origin https://github.com/yylittlecat/gitUse.git
# 将本地仓库的代码推送到远程仓库对应的分支
```



1. 本地建立一个文件夹 blog

2. cd   切换至 blog     ： cd blog

3. ~/blog$ git init    初始化仓库
   已初始化空的 Git 仓库于 /home/yz/blog/.git/

4. 添加所有变动文件，将它们从工作区放到缓存区 也就是Scurce Tree 中 暂存

   git add .

5.  推送 提交本地仓库，并填写提交的描述信息

   git commit -m "这里是本次提交的描述信息"  

6. 新见远端仓库，去对应的git 网站 新建就好了

   git remote add origin https://github.com/yz-andy/yz-andy.github.io

7. 推送

   git push -u origin master

8. 至此，本地代码和远程代码就建立连接完毕

   

9. 推送报错

   9.1、使用强制push的方法：

    git push -u origin master -f
   9.2 push前先将远程repository修改pull下来

   git pull origin master
   git push -u origin master

   9.3 若不想merge远程和本地修改，可以先创建新的分支：

   git branch [name]

   git push -u -origin[name]

   

   

   

   

   


