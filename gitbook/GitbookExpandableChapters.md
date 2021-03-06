# Gitbook 设置折叠目录 #

如果有多个目录，Gitbook在浏览器上打开时，默认所有的目录都会打开，当目录比较多时，全部显示不利于阅读。

可以使用插件配置目录折叠，使得打开浏览器时这些目录默认是关闭的。

在执行gitbook init主目录下增加book.json文件做定制化配置

配置目录折叠功能如下：

```
{
　　"plugins":[
　　　　"expandable-chapters"
　　]
}
```

然后在主目录下用命令行执行

```
$ gitbook install
```

会生成node_modules文件夹，配置的插件也会自动下载到该目录下。

在SUMMARY.md文件中配置目录时直接配置目录名称即可，不用配置连接地址，如下:

```
　　[目录名称]()
```

启动后查看即可达到预期。



除此之外，如果目录内容比较多，左边菜单栏显示不下，也可以使用插件来达到放大菜单栏宽度的目的

插件：在book.json中配置splitter，后续步骤与以上一致

　　

除了在book.json中配置外，还可以直接使用命令进行安装，如：npm install gitbook-plugin-splitter。为维护方便，推荐使用book.json文件进行配置。



更多详情,可查看 [gitbook插件官网地址](https://plugins.gitbook.com/)
