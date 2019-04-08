# Vue Design 布局

## 总体布局 ##
此项目暂定为使用Element-UI进行布局,可参看 [Element-UI 布局容器](http://element-cn.eleme.io/#/zh-CN/component/container)

- 顶部栏(24/24)
- 侧边栏(6/24)
- 主体空间(18/24)
- 底部栏(18/24)

布局图如下:
![图片](https://dev.tencent.com/api/project/4121910/files/4674418/imagePreview)

### 顶部栏设计 ###
还是按照之前做过的样式,迁移过来,大致样子为:
![图片](https://dev.tencent.com/api/project/4121910/files/4680505/imagePreview)

- 左侧为Logo,使用文字即可
- 右侧为用户信息和统一功能菜单
- 将功能菜单统一放到左侧边栏

统一的功能菜单后续再加,先完成如下:
![图片](https://dev.tencent.com/api/project/4121910/files/4686715/imagePreview)

### 侧边栏设计 ###
侧边栏设计为可以展开收缩的菜单列表,先查看 [element-ui 菜单](http://element-cn.eleme.io/#/zh-CN/component/menu)
![图片](https://dev.tencent.com/api/project/4121910/files/4687120/imagePreview)

### 底部信息栏设计 ###
底部栏暂分三个模块，使用 [element-ui card](http://element-cn.eleme.io/#/zh-CN/component/card) 组建

- 我的
- 参考
- 其他

![图片](https://dev.tencent.com/api/project/4121910/files/4688522/imagePreview)

## 效果 ##
![图片](https://dev.tencent.com/api/project/4121910/files/4689094/imagePreview)

暂决定不显示底部栏.
