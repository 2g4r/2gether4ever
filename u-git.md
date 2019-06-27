###Welcome to use My Git Knowledge

###拉取远程仓库分支  
+ `git init`在本地新建一个git仓库
+ 连接远程仓库 <br>
`git remote add 远程仓库名 '远程仓库的地址'`  
+ 连接成功之后查看远程仓库的状态   
```
git remote -v//查看当前链接的所有远程仓库

结果显示：
远程仓库1 远程仓库1的地址（fetch）
远程仓库1 远程仓库1的地址（push）
远程仓库2 远程仓库2的地址（fetch）
远程仓库2 远程仓库2的地址（push）
```  
+ 查看分支状态   
```
git branch -a 

结果显示：
本地分支1
本地分支2 
远程分支1
远程分支2
```  
+ 新建并切换分支  
```
git checkout -b 分支名
```  
+ 拉取远程分支到本地  
```
git pull 远程仓库名 远程分支名:本地分支名
```  
+ 删除某个远程仓库  
`git remote rm 远程仓库名`  
+ 删除某个远程分支  
`git push 远程仓库名 --delete 远程分支名`  
+ 删除本地分支（删除非当前所在分支的其他分支）  
`git branch -d 分支名`  
+ 删除已提交到远程的文件  
`git rm 文件名`  

### 克隆远程仓库  
+ 克隆远程仓库  
```
git clone '远程仓库名'
```  
+ 克隆仓库之后，不需要新建本地分支并进行拉取，直接切换分支即可  

#### 推送本地修改   
`git push 远程仓库 远程分支名：本地分支名`  
#### 切换到某个版本  
`git reset --hard 版本号`    
#### 远程分支退回到上次修改  
`git push origin HEAD --force`  
#### 恢复某个文件  
`git checkout -- 文件名`  
