# Git
记录一些常用的Git命令

### 一：环境准备
1、安装git客户端到自己的本地电脑 不同系统各自安装，通过git --version来确认是否安装完成，Windows通过右键查看是否多出git bash选项

2、在github上注册一个账号

3、在本地电脑和git配置无密钥登录，自行配置，将.ssh目录下id_rsa内容拷贝至githubssh-key进行配置

4、创建本地版本库
新建一个文件夹，后续里面的文件需要和远程同步、新建好后，初始化
git init，会出现一个隐藏文件夹.git，该文件夹在的区域代表该区域是工作区

### 二：概念性术语
1、工作区、暂存区、版本库
工作区就是包含.git的工作目录
暂存区表示暂时保管文件区域 在.git目录的index文件
版本库表示.git文件夹，版本库

工作目录下文件 通过git add放到暂存区
暂存区文件 通过git commit -m 放到版本库

### 三：常见操作对应的命令
1、单个分支常见操作：
克隆、推送、拉取、回退版本、查看日志
从远程库克隆版本：git clone xxxxxx
推送：把本地问题版本推送到远程库p:git push origin master
拉取：拉取远程库上最新的代码：git pull 
查看日志：git log
查看每步操作的id：git reflog
回退版本：git reset --hard head_id/HEAD


2、多分支管理常见操作
创建分支并切换到该分支
git checkout -b fenzhi001

相当于：
1、创建分支 git branch dev
2、切换分支 git checkout dev

切换分支
git checkout branch001

删除分支

合并分支
git merge branch001


解决分支冲突
需要手动修改冲突的地方，然后add后commit提交到版本库
