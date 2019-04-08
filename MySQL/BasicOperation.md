# MySQL 基本操作

## 登陆 ##
MySQL登陆命令格式如下,当在本机运行时,可省略 -h 选项.

> mysql -h 主机名 -u 用户名 -p
> Enter password:

打开 windows命令行工具, 切换到mysql解压目录,然后执行:

```
D:\tools\mysql-8.0.15-winx64\bin>mysql.exe -u root -p
Enter password: ************
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 8
Server version: 8.0.15

Copyright (c) 2000, 2019, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql>
```

此时已经登陆MySQL.

输入 `exit` 或 `quit` 命令,即可退出登陆.

## 使用命令修改密码 ##

```
D:\tools\mysql-8.0.15-winx64\bin>mysql.exe -uroot -p
Enter password: ***********
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 11
Server version: 8.0.15 MySQL Community Server - GPL

Copyright (c) 2000, 2019, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> ALTER user 'root'@'localhost' IDENTIFIED BY 'new_password';
Query OK, 0 rows affected (0.04 sec)

mysql>
```


## 使用数据库辅助工具修改密码 ##

### Navicat ###
打开navicat,并连接数据库:
![图片](https://dev.tencent.com/api/project/4121910/files/4722065/imagePreview)

点击工具栏中的 **用户** ,就可以查看所有的mysql用户
![图片](https://dev.tencent.com/api/project/4121910/files/4722066/imagePreview)

双击要修改密码的用户,输入新密码,点击保存即可
![图片](https://dev.tencent.com/api/project/4121910/files/4722069/imagePreview)
