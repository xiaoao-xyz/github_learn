## Lesson-5


### 全局设置
  * git config --global user.name 'xiaoao-xyz'
  * git config --global user.email "×××××@××××.××"
  **在commit的时候会提醒你加**
  
### 删除文件
  * 先从工作区，即系统目录中删除
  * 再在git中删除 git rm filename (忽略第一步貌似也行，结果一样) 
  * commit
  * 注意任何一种删除结果都不会出现在回收站中
  
### 克隆
   git clone ××××××.git
   
### 上传
   git push
   会要求你输入帐号密码，但是双因子认证貌似不可以直接用帐号密码授权
   **可以**
