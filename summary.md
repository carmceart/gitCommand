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

