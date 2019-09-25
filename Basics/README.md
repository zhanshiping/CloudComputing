**一、购买腾讯云服务器并登录**

1、购买腾讯云服务器（学生套餐）

![](../Basics images/1.png)

2、使用Web Shell登录已购买的云服务器实例

![](../Basics images/48.png)

3、下载安装Xshell（包含在Xmanager中），并使用Xshell登录腾讯云实例

![](../Basics images/2.png)

![](../Basics images/3.png)

**二、创建GitHub项目并在本地同步**

1、注册GitHub账号：https://github.com/

![](../Basics images/4.png)

2、在GitHub上创建云计算项目（CloudComputing）并在本地同步

2.1创建SSH Key

2.1.1验证是否存在ssh keys：ls -al ~/.ssh

![](../Basics images/49.png)

2.1.2创建新的ssh key
如果不存在ssh密钥，则新建一个： ssh-keygen -t rsa -b 4096 -C “your_email@example.com”

your_email@example.com替换成你的Github邮箱地址

![](../Basics images/5.png)

在“C:\Users\UserName”文件夹下就会创建.ssh文件夹，文件夹中生成“id_rsa”和“id_rsa.pub”两个文件，分别对应私钥和公钥。

![](../Basics images/6.png)

复制“id_rsa.pub”的内容到GitHub网站的Settings–>SSH and GPG keys中：

![](../Basics images/7.png)

2.2测试SSH Key是否配置成功：ssh -T [git@github.com](mailto:git@github.com)

![](../Basics images/8.png)

3、配置GitHub的用户名和邮箱

3.1

配置用户名：git config --global user.name “zhanshiping”

配置邮箱：git config --global user.email “313718626@qq.com”

![](../Basics images/9.png)

4、创建GitHub项目并在本地进行同步

4.1访问GitHub网站并新建代码仓库

![](../Basics images/10.png)

4.2创建本地代码仓库

4.2.1首先在本地规划好一处文件夹用于同步GitHub的项目，然后打开Git Bash，定位到此次你想要同步的GitHub项目的文件夹，使用“cd”命令。

![](../Basics images/11.png)



![](../Basics images/12.png)

4.2.2初始化本地文件夹作为一个Git仓库：git init

![](../Basics images/13.png)

4.2.3拷贝GitHub网站中的项目网址：

![](../Basics images/14.png)

4.2.4添加远程代码仓库的URL：

```
git remote add origin https://github.com/zhanshiping/CloudComputing.git
```

![](../Basics images/15.png)

4.2.5验证一下添加是否成功：git remote -v

![](../Basics images/16.png)

4.2.6首先从远程代码仓库拉取数据:git pull origin master

![](../Basics images/17.png)

4.2.7新建README文档:touch README.md

![](../Basics images/18.png)

4.2.8添加文件夹中的所有文件: git add

![](../Basics images/19.png)

4.2.9提交文件：git commit -m “First commit”

![](../Basics images/20.png)

4.2.10推送本地更新至远程服务器：git push -u origin master

![](../Basics images/21.png)

三、本地安装VMware Workstation和CentOS操作系统

1、安装VMware WorkStation（由于很早以前就安装了，无截图）

![](../Basics images/22.png)

2、安装Centos

2.1下载centos镜像

![](../Basics images/23.png)

2.2新建虚拟机

![](../Basics images/24.png)

![](../Basics images/25.png)

![](../Basics images/26.png)

![](../Basics images/27.png)

![](../Basics images/28.png)

![](../Basics images/29.png)

![](../Basics images/30.png)

![](../Basics images/31.png)

![](../Basics images/32.png)

![](../Basics images/33.png)

![](../Basics images/34.png)

![](../Basics images/35.png)

![](../Basics images/36.png)

![](../Basics images/37.png)

2.3编辑虚拟机设置

![](../Basics images/38.png)

![](../Basics images/39.png)

2.4开启虚拟机

![](../Basics images/40.png)

![](../Basics images/41.png)

![](../Basics images/42.png)

![](../Basics images/43.png)

![](../Basics images/44.png)

![](../Basics images/45.png)

![](../Basics images/46.png)

![](../Basics images/47.png)

2.5重启完成安装