# Java Debug 中文乱码

指定编码

```
$ javac -encoding UTF-8 XXX.java
```

当使用java命令时,会遇到中文乱码的问题,可以执行以下命令:

```
$ export JAVA_TOOL_OPTIONS=-Dfile.encoding=UTF8
```

再执行java命令即可.

```
$ java XXX
```
