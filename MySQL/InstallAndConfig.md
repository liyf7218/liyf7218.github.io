# MySQL 安装配置

以下内容源自 [菜鸟教程 MySQL安装](http://www.runoob.com/mysql/mysql-install.html)

### 下载 ###
所有平台的 MySQL 下载地址为： [MySQL 下载](https://dev.mysql.com/downloads/mysql/)
以下以Windows安装为例:
打开网址,选择要下载的安装包:
![图片](https://dev.tencent.com/api/project/4121910/files/4717010/imagePreview)

选择不登陆,直接下载:
![图片](https://dev.tencent.com/api/project/4121910/files/4717022/imagePreview)

### 安装配置 ###
将下载好的压缩包解压到 D:\tools\mysql-8.0.15-winx64 目录下,再进行后续操作.

#### 接下来我们需要配置下 MySQL 的配置文件 ####
打开刚刚解压的文件夹 D:\tools\mysql-8.0.15-winx64 ，在该文件夹下创建 my.ini 配置文件，编辑 my.ini 配置以下基本信息：

```
[mysql]
# 设置mysql客户端默认字符集
default-character-set=utf8

[mysqld]
# 设置3306端口
port = 3306
# 设置mysql的安装目录
basedir=D:\\tools\\mysql-8.0.15-winx64
# 设置 mysql数据库的数据的存放目录，MySQL 8+ 不需要以下配置，系统自己生成即可，否则有可能报错
# datadir=D:\\tools\\sqldata
# 允许最大连接数
max_connections=20
# 服务端使用的字符集默认为8比特编码的latin1字符集
character-set-server=utf8
# 创建新表时将使用的默认存储引擎
default-storage-engine=INNODB
```

#### 启动下 MySQL 数据库 ####
***以管理员身份打开*** windows命令行工具 (C:\Windows\System32\cmd.exe),切换到mysql的解压目录

```
$ C:\WINDOWS\system32>D:
$ D:\>cd tools
$ D:\tools>cd mysql-8.0.15-winx64
$ D:\tools\mysql-8.0.15-winx64>cd bin
$ D:\tools\mysql-8.0.15-winx64\bin>
```

初始化数据库

```
$ mysqld.exe --initialize --console
2019-03-04T11:24:45.451166Z 0 [System] [MY-013169] [Server] D:\tools\mysql-8.0.15-winx64\bin\mysqld.exe (mysqld 8.0.15) initializing of server in progress as process 1696
2019-03-04T11:24:45.454317Z 0 [Warning] [MY-013242] [Server] --character-set-server: 'utf8' is currently an alias for the character set UTF8MB3, but will be analias for UTF8MB4 in a future release. Please consider using UTF8MB4 in order to be unambiguous.
2019-03-04T11:24:49.886106Z 5 [Note] [MY-010454] [Server] A temporary password is generated for root@localhost: o_5cRs?ckQn7
2019-03-04T11:24:51.420665Z 0 [System] [MY-013170] [Server] D:\tools\mysql-8.0.15-winx64\bin\mysqld.exe (mysqld 8.0.15) initializing of server has completed
```

其中, ` o_5cRs?ckQn7` 就是初始密码,后续登陆需要用到,你也可以再登陆后修改密码
输入以下安装命令:

```
$ mysqld.exe install
Service successfully installed.
```

启动输入以下命令即可:

```
C:\WINDOWS\system32>net start mysql
请求的服务已经启动。

请键入 NET HELPMSG 2182 以获得更多的帮助。
```
