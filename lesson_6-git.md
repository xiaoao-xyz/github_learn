### Lesson_6  分支与回滚

#### 分支
1. 查看分支

`git branch`
        
        加 -a 可以查看远程代码分支
    
    
2. 创建分支并转到

`git checkout -b branchname`
    
        相当于 
    
`git branch branchname`
    
`git checkout branchname`
    

 3. 提交到远程
 
`git push origin branchname`
        
        如果远程仓库没有branchname会自动创建一个
        
`git push origin branchname:master`
        
        提交到制定分支,如master
        
        所以 branchname 所占的位置代表要提交的本地仓库,如果后面不加:targetname,即认为是与之相对应的远程仓库
        
        origin是代表本主机?
        origin就是一个名字，它是在你clone一个托管在Github上代码库时，git为你默认创建的指向这个远程代码库的标签
        可以通过
        'git remote -v'
        查看
        详情参看
        https://blog.csdn.net/biqioso/article/details/81140711?utm_source=blogxgwz6&spm=1018.2118.3001.4187
        

#### 标签
1. 打上标签

`git tag -a tagname -m "msg" commit_id`
                        
        其中commit_id如果省略表示标记当前分支
        
        这个标签可以被校验，可以轻量化为
        
`git tag tagname commit_id`

        创建时添加标签
`git checkout -b branchname tagname`
        
2. 推送到远程仓库

`git push origin tagname`
                
         一次性推出
           
`git push origin --tags`

3. 删除标签

`git tag -d tagname`

        远程删除
      
`git push origin :refs/tags/tagname`





#### 回滚
1. 查看版本号

`git log`
    
        按q退出
      
2. 切换到历史版本

`git reset --hard commit_id`
        
        退回到上一个版本
        
`git reset --hard HEAD^`
        
        上上一个版本
        
`git reset --hard HEAD^^`
       
3. 工作区修改了并且还没有提交情况下的恢复

`git checkout filename`

        
4. 提交到了缓存区的恢复
        
  `git reset HEAD filename`
`git checkout filename`
**如果缓存区存在修改了的对应的文件，那么是从缓存区恢复这个文件的版本**
        
        第一步可不可以用(应该可以)
`git rm --cached .`
        
 
        
        
        
    


