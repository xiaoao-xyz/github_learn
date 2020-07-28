### the rest point

1. 合并

  `git checkout master`
  
  `git merge branch_name`
  
  
  `git checkout branch_name`
  
  `git rebase master`
  
  **rebase是将分支对分支与主干的共同祖先的修改，对此时的主干做相同的操作**
  **它这个操作创建了一个分支副本，与之前的分支不同之处是，它的祖先变成了当前的master**
  **还需要操作接下来两步才能达到merge同样的效果，也叫前向合并(fast-forward merge)**
  `git checkout master`
  `git merge branch_name`

#### 问题:
  1. rebase的意义在哪？
  2. rebase的冲突理应也存在
            
          是的，处理完冲突后
          
          git rebase --continue
          
          放弃
          
          git rebase --abort
          
          直接用branch_name代替
          git rebase --skip
          

  
   [详情参看](https://blog.csdn.net/iteye_4921/article/details/82639094?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-2.channel_param&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-2.channel_param)
  
2. 暂存


`git stash save`

        想删掉一段代码又担心以后需要查看它
        
        想保存它但又不想增加一个脏的提交
        

       
        
