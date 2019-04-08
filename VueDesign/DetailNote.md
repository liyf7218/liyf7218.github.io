# Vue Design 详细设计 笔记

### 用于每日记录,或者随笔记录 ###
功能如下

- 添加新的记录,内容至少包括:
    - 标题
    - 日期
    - 内容
- 列表/修改/删除
- 按照关键字搜索

### 展示 ###
使用 [element-ui card组件](http://element-cn.eleme.io/#/zh-CN/component/card) 进行组织
标题,日期在上,内容在下
![图片](https://dev.tencent.com/api/project/4121910/files/4697182/imagePreview)

### 功能实现 ###

#### 按钮和搜索框 ####
在顶部添加统一功能按钮
![图片](https://dev.tencent.com/api/project/4121910/files/4696579/imagePreview)
在每条信息中添加各自按钮
![图片](https://dev.tencent.com/api/project/4121910/files/4696582/imagePreview)

#### 弹出框 ####
当点击新增或是修改按钮时,需要弹出form表单,捡起放在弹出框中
![图片](https://dev.tencent.com/api/project/4121910/files/4696844/imagePreview)
当点击查看按钮,或是点击卡片本身时,弹出详情展示框
![图片](https://dev.tencent.com/api/project/4121910/files/4696587/imagePreview)
当点击删除按钮时,需要弹出确认框
![图片](https://dev.tencent.com/api/project/4121910/files/4696665/imagePreview)
