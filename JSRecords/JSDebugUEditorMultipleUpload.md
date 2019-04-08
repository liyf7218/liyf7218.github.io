# JS DEBUG UEditor多图上传报错

## 多图上传报错 ##

查看 [ueditor报错because its MIME type ('text/html') is not a supported stylesheet MIME type, and strict MIM](https://blog.csdn.net/qq_33769914/article/details/84942208)

原文如下:

------

点击图片工具的时候报错如下:

![图片](https://dev.tencent.com/api/project/4121910/files/4689778/imagePreview)

点开发现是一个image.html的页面但是具体也没有哪里的报错。

因此我全局搜索了dialogbase.css这个内容。发现

![图片](https://dev.tencent.com/api/project/4121910/files/4689783/imagePreview)

我想可能是下面的rel的问题，把他隐藏

![图片](https://dev.tencent.com/api/project/4121910/files/4689786/imagePreview)

然后好啦。

-----
