# IDEA Debug 中文乱码

### IntelliJ IDEA 统一设置编码为utf-8编码 ###
查看 [CSDN IntelliJ IDEA 统一设置编码为utf-8编码](https://blog.csdn.net/fengqing5578/article/details/80648753)

### 启动项目时输出信息乱码 ###
- 特征值

    [淇℃伅 [main] org.apache.catalina.startup.VersionLoggerListener.log Server.鏈嶅姟鍣ㄧ増鏈�:]
    
- 原因

    tamcat输出日志的设定编码不识别对应的字符

- 解决办法

    查看 [CSDN 解决tomcat乱码](https://blog.csdn.net/fjh19950514/article/details/88525201)
    实际操作:到 tomcat/conf/ 目录下,修改 logging.properties 找到 `java.util.logging.ConsoleHandler.encoding = utf-8` 这行 更改为 `java.util.logging.ConsoleHandler.encoding = GBK`
