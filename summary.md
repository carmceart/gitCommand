# git常用命令总结

#### 初始化

git init

#### 添加文件

git add .

#### 代码提交

git commit -m "first commit"

#### 远程同步
git remote add origin git@github.com:cctohly/gitCommand.git
git push -u origin master



# 解决问题

#### 1.撤销git add提交的文件

###### 1. 错误提交

touch read.md

git add read.md

###### 2. 查看暂存区文件

git ls-files

>--cached(-c)显示暂存区中的文件，git ls-files命令默认的参数
>
>--deleted(-d)显示删除的文件
>
>--modified(-m) 显示修改过的文件
>
>--other(-o)显示没有被git跟踪的文件
>
>--stage(-s) 显示mode以及文件对应的Blob对象，进而我们可以获取暂存区中对应文件里面的内容

###### 3. 删除暂存区中的文件(停止追踪,但保留在工作区)

git rm --cached [file] 

###### 4. 小心得

git add 后,所有的add的文件改变会被git追踪(即放到了暂存区)

#### 2.git commit报错Changes not staged for commit:

虽然add 后的所有文件会被追踪,但是提交前都必须再先git add一次   

可使用命令来完成add+提交

git commit -am "message"

> -a 表示 add                        

#### 3.谨慎使用git rm -f 删除文件后只能退回版本找回

#### 4.删除远程仓库

显示所有远程仓库  
git remote -v

增加一个新的远程仓库，并命名  
git remote add [shortname] [url] 

删除一个远程仓库

git remote rm [shortname]



