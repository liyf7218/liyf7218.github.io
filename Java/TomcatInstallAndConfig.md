# Java Tomcat安装配置

## 下载 ## 
[Tomcat 官网](http://tomcat.apache.org/)
[Tomcat 下载地址](https://tomcat.apache.org/download-90.cgi)

## 测试是否可用 ##
将压缩包解压出来,进入目录 `unzipDir/bin/` ,运行 startup.bat(.sh)

```
// windows 使用双击即可,其他可使用命令
$ ./startup.sh
```

此时会提示服务在xxxms内启动,使用浏览器打开 [http://localhost:8080](http://localhost:8080), 看到以下页面,说明可运行
![图片](https://dev.tencent.com/api/project/4121910/files/4710439/imagePreview)

## 解压和配置 ##
将Tomcat压缩包解压到指定目录,暂指定 `D:\tools\apache-tomcat-9.0.16\` ,然后进行环境变量配置
右击 “我的电脑” -> 点击”属性” -> “高级系统设置” -> “高级”选项卡 -> “环境变量”
添加(若已存在则编辑追加)一下环境变量:
- CATALINA_BASE -> D:\tools\apache-tomcat-9.0.16
- CATALINA_HOME -> D:\tools\apache-tomcat-9.0.16
- CLASSPATH -> %CATALINA_HOME%\lib\servlet-api.jar;
    ![图片](https://dev.tencent.com/api/project/4121910/files/4710416/imagePreview)
- PATH -> %CATALINA_HOME%\bin;%CATALINA_HOME%\lib;
    ![图片](https://dev.tencent.com/api/project/4121910/files/4710407/imagePreview)

## 测试是否配置成功 ##
打开命令行工具,输入命令

```
$ startup
```
同样打开浏览器,输入 [http://localhost:8080](http://localhost:8080), 看到以下页面,说明可运行.图片同上.

> 请勿执行 `shutdown` 命令!
