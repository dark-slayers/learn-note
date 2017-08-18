# Git常用命令：
---
### 查看目前状态：
git status

---
### 将目前目录中的全部文件添加至Git控制：
git add –A

---
### 将过滤规则中的文件夹从GIT管理中去除：
git clean -f -d

---
### 提交：
git commit -m "描述信息"

---
### 查看文件前后区别：
git diff

---
### 查看提交日志：
git log<br>
git log -n

---
### 查看过去的命令
git reflog

---
## 版本更换：
### 切换至上个版本：
git reset --hard HEAD^
### 切换至ID以3628164开头的版本：
git reset --hard 3628164

---
### 从远程库克隆：
***克隆Google的android系统Camera2演示***<br>
git clone git@github.com:googlesamples/android-Camera2Basic.git<br>
***克隆hosts文件项目***<br>
git clone git@github.com:racaljk/hosts.git

---
### 同步hosts项目
git pull racaljk master
### 将同步后的项目推送至自己的github库
git push

---
### 拉取远程origin分支并且合并到本地master分支
git pull origin master

---
### 将修改推送至Github
***首次推送***<br>
git push -u origin master<br>
***推送***<br>
git push origin master

---
### 安装GitShell快捷方式
使用客户端打开GitShell<br>
github --reinstall-shortcuts<br>

---
### 查看全部配置信息
git config --list
### 查看用户名和邮箱地址：
git config user.name<br>
git config user.email
### 修改用户名和邮箱地址：
1. 全局<br>
git config --global user.name "username"<br>
git config --global user.email "email"<br>
2. 项目<br>
git config user.name "username"<br>
git config user.email "email"<br>
---
### 创建分支
git checkout -b dev
### 切换回主分支,将dev分支的改动合并入主分支：
git checkout master<br>
git merge dev
### 再把新建的分支删掉：
git branch -d dev
### 除非你将分支推送到远端仓库，不然该分支就是 不为他人所见的：
git push origin <branch>
---
