# Java 安装配置

摘自 [菜鸟教程 Java开发环境配置](http://www.runoob.com/java/java-environment-setup.html)

只概述Windows下的安装配置

### 安装 ###
先 [下载JDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html)

### 配置 ###
安装完成后:
右击 "我的电脑" -> 点击"属性" -> "高级系统设置" -> "高级"选项卡 -> "环境变量"

添加(若以存在则编辑)一下环境变量:

- JAVA_HOME -> C:\Program Files\Java\jdk1.8.0_201    //要根据自己的实际路径配置
- CLASSPATH -> .;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;         //记得前面有个"."
- Path -> %JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;

![图片](https://dev.tencent.com/api/project/4121910/files/4709821/imagePreview)

> 注意：如果使用1.5以上版本的JDK，不用设置CLASSPATH环境变量，也可以正常编译和运行Java程序。

### 测试是否安装成功 ###
"开始" -> "运行" -> 键入"cmd" -> 运行以下命令

```
$ java -version
// 以下出现版本号时,表明安装成功
java version "1.8.0_201"
Java(TM) SE Runtime Environment (build 1.8.0_201-b09)
Java HotSpot(TM) 64-Bit Server VM (build 25.201-b09, mixed mode)
```
