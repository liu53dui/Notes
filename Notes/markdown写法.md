使用vscode写好markdown
插件
    markdown all in one 很多快捷键很补全的操作
    markdown preview enhanced 可以边写markdown边看到你写出来的样子
    paste image 可以方便的把图片插入到markdown中
    LimfxCodeEx 可以快速的把文章发表到limfx上
    code spell checker 快速拼写检查

# 这是一级标题
## 这是二级标题
### 这是三级标题
换行但是不另起一段的话在后面加两个空格(后面有两个空格)  
这里的换行就比较接近

如果换行另起一段的话需要隔一行

就像这样

强调 **加粗了**  *变斜了*

有序列表
1. 有序列表
   1. 小内容
      1. 小小内容
2. 有序列表2

复制图片的粘贴的话是使用 ctrl+alt+v
如果是已经在文件夹里的图片使用的话，直接使用
![](括号里是图片地址)

# 公式输入的话直接使用上下两个$符号

$$
\lim_{x\to\infin}\frac{sin(t)}{x}=1
$$
这个公式是独占一段的

但是也可以在一段文字中插入公式，ctrl+m， $\lim_{x\to\infin}\frac{sin(t)}{x}=1$


# 表格
第一行是表头用|隔开
第二行是代表每一行里面的文字是朝左还是朝右，朝左就在左边加冒号，朝右就在右边加冒号，居中就是两边都加,默认左对齐
在文本中不是很好看的话就可使用alt+shift+f格式化

| 小明 | 小王  | 小张 |
| ---: | :---: | :--- |
|    1 |   2   | 3    |


# 插入链接
直接复制过来然后点击鼠标左键选中你想要的链接的文字

# 代码块
可以指定语言
```javascript
var s = 'this is code'
alert(s)
```

那么我们想把md导出的话，那我们使用的就是markdown preview enhanced，这个导出的话可以保证导出的公式格式是对的。导出的话我们在预览的情况下点右键，然后Chrome选择格式

如果我们想要发表在limfx上我们只有点右边的小图标就好

[其他补充内容](https://www.limfx.pro/ReadArticle/57/yi-zhong-xie-zuo-de-xin-fang-fa)
[补充笔记，包括写法等](https://blog.csdn.net/qq_43732429/article/details/108034518)
