# CSS 隐藏滚动条

## 隐藏滚动条 ##
查看 [CSS 元素超出部分滚动, 并隐藏滚动条](https://www.cnblogs.com/lovling/p/8000363.html)
设置样式：

```
<style>
    #box {
        width: 500px;
        height: 300px;
        overflow-x: hidden;
        overflow-y: scroll;
        line-height: 30px;
        text-align: center;
    }
    #box::-webkit-scrollbar {
        display: none;
    }
</style>
```
