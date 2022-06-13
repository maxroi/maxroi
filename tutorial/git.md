# 使用git
新建repo目录，新建demo.md文件，进入其中
1. 初始化  
  git init
2. 查看状态   
  git status
3. 添加追踪文件，到缓冲区  
  git add demo.md （如果是添加目录，demo/）
4. 提交到仓库，注释信息是change file   
  git commit -m "change file"
5. 查看日志   
  git log
6. 查看分支情况   
  git branch
7. 新建分支first  
  git branch first
8. 切换到first分支   
  git checkout first
9. 在当前分支，合并first分支  
  git merge first
10. 删除first分支，强制删除用-D   
  git branch -d first
11. 为当前分支添加标签v1.0   
  git tag v1.0
12. 查看标签情况  
  git tag
13. 切换到v1.0标签分支   
  git checkout v1.0

# 绑定git与github
如果已经安装git，默认安装了ssh  
1. 查看是否已安装ssh  
  ssh   
2. 生成密钥  
  ssh-keygen -t rsa （私钥id_rsa公钥id_rsa.pub，默认位置C:\Documents and Settings\username\.ssh）  
3. 添加到github   
  将公钥id_rsa.pub的内容粘贴到Key处   
4. 验证  
  ssh -T git@github.com

# 通过git提交代码到github
1. 把本地代码推到远程仓库   
  git push origin master  
2. 把远程仓库拉到本地   
  git pull origin master  
3. 为了不造成冲突，在push操作前先进行pull操作

# clone仓库到本地
一.本地没有该仓库，可直接将远程仓库clone到本地，此时通过命令创建的本地仓库不用再进行初始化操作，且自动关联远程仓库    
1. git clone 远程仓库clone地址

二.本地已有仓库，并且已进行过多次commit操作   
1. 新建一个仓库，初始化    
2. 关联远程仓库    
  git remote add origin 远程仓库clone地址 （其中为远程仓库命名为origin，如果需关联多个远程仓库，要分别命名）    
3. 同步远程和本地仓库   
  git pull origin master
