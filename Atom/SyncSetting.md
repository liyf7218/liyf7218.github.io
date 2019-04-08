# Atom 配置 sync-setting

## 我的配置项 ##
gistId:

`acd3ce8dfd2b80e52da7d6bd041873e4`

token:

`dec5fc15f37cc0740727a69d34b105f739026c12`

## Atom 通过sync-settings插件实现同步功能 ##
查看 [简书 Atom 通过sync-settings插件实现同步功能](https://www.jianshu.com/p/fb8eda173e81)
查看 [atom.io sync-setting](https://atom.io/packages/sync-settings)

### 准备 ###
- 安装Atom
- 安装 sync-setting 插件
- 有一个GitHub账号

### 步骤 ###
安装sync-setting插件,打开Atom的Setting页面,点击 install,输入要安装的包
![图片](https://dev.tencent.com/api/project/4121910/files/4764870/imagePreview)

打开sync-settings插件设置，你会看到如下界面
![图片](https://dev.tencent.com/api/project/4121910/files/4764792/imagePreview)

- 我们只需要填入Token以及Gist Id即可（红框标出部分）
    - 每台电脑的Token可以相同也可以不同，不过Token只能看见一次，所以你需要自己保存起来
    - 每台电脑的Gist Id都是相同的，因为你的数据都存放在Gist上。
    - 其他的是一些自定义选项，比如是否需要同步快捷键之类的，建议默认就好。

按下Ctrl-Shift-P打开命令面板
![图片](https://dev.tencent.com/api/project/4121910/files/4764809/imagePreview)

输入 sync-settings:backup 将本机配置上传到gist，成功后如图：
![图片](https://dev.tencent.com/api/project/4121910/files/4764813/imagePreview)

输入 sync-settings:restore 将gist上的配置同步到本机，成功后如图：
![图片](https://dev.tencent.com/api/project/4121910/files/4764819/imagePreview)

### 如何设置Token ###
登录GitHub，点击你的头像 => 点击settings => 点击Personal access tokens => 点击Generate new token
![图片](https://dev.tencent.com/api/project/4121910/files/4764826/imagePreview)

随便起一个名字，再将所有的选项全部勾上
![图片](https://dev.tencent.com/api/project/4121910/files/4764827/imagePreview)

点击Generate token创建
![图片](https://dev.tencent.com/api/project/4121910/files/4764831/imagePreview)

将刚生成的Token复制到sync-settings中
![图片](https://dev.tencent.com/api/project/4121910/files/4764833/imagePreview)

注意：Token生成后只能看见一次，如果关闭页面后再次打开就看不见了。

### 如何设置Gist Id ###
登录GitHub，点击Gist
![图片](https://dev.tencent.com/api/project/4121910/files/4764844/imagePreview)

在新版面的github中,点击 头像 -> Your gists
![图片](https://dev.tencent.com/api/project/4121910/files/4764848/imagePreview)

> 此时,可能会发现 [https://gist.github.com](https://gist.github.com) 被墙了,可以按照以下方法解决:
> windows下 打开C:\Windows\System32\drivers\etc\hosts文件
> 编辑器打开，在最后行添加192.30.253.118 gist.github.com
> 保存, over~

里面随便写一些内容，然后点击创建
![图片](https://dev.tencent.com/api/project/4121910/files/4764875/imagePreview)

创建完成后，将网址冒号后面的内容复制到sync-settings里
![图片](https://dev.tencent.com/api/project/4121910/files/4764879/imagePreview)

两项都设置完成后如下图：
![图片](https://dev.tencent.com/api/project/4121910/files/4764885/imagePreview)

至此,设置完成.
