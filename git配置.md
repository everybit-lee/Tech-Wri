#git安装及配置

## 客户端安装及配置

### 安装

[下载git for windows](https://gitforwindows.org/)

[安装TortoiseGit客户端程序](https://tortoisegit.org/download/)
这两个傻瓜式安装即可

----**课程教学软件下载请看 softbak 文件夹中说明文件**----



TortoiseGit的操作集成在右键菜单中

可在首次运行时进行全局配置，包括生成客户端密钥对、指定用户名及邮箱等

=======




### 配置要点

#### 配置本地仓库

两种方式：

1、从远端clone仓库到本地

=======
1、从远端clone仓库到本地

2、在本地建仓库

#### 配置远程访问参数

1、密钥生成及管理

运行命令来配置你的用户名和邮箱：
> $ git config --global user.name "superGG1990"
> $ 
>
> git config --global user.email "superGG1990@163.com"
>

git支持https和git两种传输协议，github分享链接时会有两种协议可选：

git协议链接图例 : ↓

![img](https://images2015.cnblogs.com/blog/1160195/201705/1160195-20170512104128676-1577931353.png)

*https协议链接图例：\**↓***

![img](https://images2015.cnblogs.com/blog/1160195/201705/1160195-20170512104128676-1577931353.png)

git使用https协议，每次pull, push都会提示要输入密码，使用git协议，然后使用ssh密钥，这样免去每次都输密码的麻烦

生成密钥对

```
$ ssh-keygen -t rsa -C "your_email@youremail.com"

Creates a new ssh key using the provided email # Generating public/private rsa key pair.

Enter file in which to save the key (/home/you/.ssh/id_rsa):
```

1.1 [在tortoise中生成密钥---百度知道图文解答](https://jingyan.baidu.com/article/495ba841f2892638b30edefa.html)



1.2 让服务器识别你——将密钥加入服务器

	将自己的公钥文件发送给git管理员，由管理员将你的公钥写入Git服务器相应文件中

2、远端克隆、提交等及提交需要的参数

主要有两个：你的密钥（服务器验证）和库所在URL

####如何让git小乌龟工具TortoiseGit记住你的账号密码
在使用小乌龟的过程中，发下每次push或者pull都要重复输入账号密码，非常麻烦。
如果能记住账号密码就好了，这样就省去了时间。

#######怎么设置记住密码
在[系统盘]:\Users[你的用户名]下面，有一个.gitconfig目录，这个是记录你的git配置信息的。
在该文件后面加上

>[credential]
>​    helper = store
保存后。试一下pull或者push，就会在[系统盘]:\Users[你的用户名]目录下面生成
.git-credentials文件，该文件明文记录了你输入的账号密码

>http://username:password@git.llpp.com  

--------

### 常规操作 (TortoiseGit)


#### 从服务器克隆/拉取数据

#### 向本地库/服务器库提交数据
=======
#### 从服务器拉取数据

#### 向服务器提交数据


#### 分支与合并


## 服务器端配置

### 安装git

### 配置远程库及管理用户

### 配置客户访问
