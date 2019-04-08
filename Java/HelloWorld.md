# Java HelloWorld

### 基本语法 ###
编写Java程序时，应注意以下几点：

- 大小写敏感：Java是大小写敏感的，这就意味着标识符Hello与hello是不同的。
- 类名：对于所有的类来说，类名的首字母应该大写。如果类名由若干单词组成，那么每个单词的首字母应该大写，例如 MyFirstJavaClass 。
- 方法名：所有的方法名都应该以小写字母开头。如果方法名含有若干单词，则后面的每个单词首字母大写。
- 源文件名：源文件名必须和类名相同。当保存文件的时候，你应该使用类名作为文件名保存（切记Java是大小写敏感的），文件名的后缀为.java。（如果文件名和类名不相同则会导致编译错误）。
- 主方法入口：所有的Java 程序由public static void main(String []args)方法开始执行

### 创建一个新的java文件 ###
新建文件 HelloWorld.java , 内容如下:

```
public class HelloWorld {
    public static void main(String []args) {
        System.out.println("Hello World !");
    }
}
```

### 编译运行 ###
打开命令行,切换到此工作目录,然后执行以下操作

```
$ javac HelloWorld.java
// 此时,工作目录中会出现一个名为 HelloWorld.class 的文件,这是编译过的Java文件
$ java HelloWorld
// 注意,使用java命令时,后接类名即可,不要带后缀
Hello World
```

打印出 "Hello World !" 字样,表明第一个java文件运行成功.
