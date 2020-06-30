## MarkDown的部分语法 + VScode插件 书写 GitHub 上的 pages

## 1.1 安装 VScode + Markdown 增强插件
vscode默认是支持Markdown的，但是我们还是需要一些额外的插件来辅助。如前文安装中文包一般，到vscode的插件市场中，搜索Markdown关键字，安装这几个插件：

>![Anti](https://pic1.zhimg.com/80/v2-041bac2e2ebb23eb59ea9b74f5bc825c_720w.jpg)
>![Anti](https://pic2.zhimg.com/80/v2-622728bdbd3b0155bf205f018c7d983d_720w.jpg)

第一个插件，是一个组合包，一股脑把最常用的Markdown优化都给你装好；第二个插件，则是Github使用的Markdown渲染样式，不是特别华丽，很朴素，很简洁的样式，因为很多人用Markdown都是为了使用Github Pages，所以这个样式特别受欢迎。使用这个样式，在本地就能预览Markdown文件最终在Github Pages中显示的效果。

## Markdown 的基本语法
## 2.1 标题
两种形式：  
1）使用`=`和`-`标记一级和二级标题。
> 一级标题   
> `=========`   
> 二级标题    
> `---------`

效果：
> 一级标题   
> =========   
> 二级标题
> ---------  

2）通过`#`字符来规定标题(符号和文本之间需要隔开一个字符),可扩展6级标题
> \# 一级标题   
> \## 二级标题   
> \### 三级标题   
> \#### 四级标题   
> \##### 五级标题   
> \###### 六级标题    

效果：
> # 一级标题   
> ## 二级标题   
> ### 三级标题   
> #### 四级标题   
> ##### 五级标题   
> ###### 六级标题

## 2.2 正文
正文的内容像现在的文字一样直接输出就行，注意一点的是：MarkDown的段落换行需要实际的空一行出来才能生效。

## 2.3 代码块
代码块通过两行 ``` 符号框出，如果你写的代码是某种语言，那么可以在第一行末尾加上这个语言的名字，代码块内的代码就会执行对应的高亮语法，例如python

\```python

> private static int updateDesktop(Image wallpaper){    
> int happiness;    
> MyDesktop desktop = new MyDesktop();\
> desktop.apply(wallpaper);   
> happiness = INFINITY;   
> return happiness;   
> }

\```

效果：
```python
private static int updateDesktop(Image wallpaper){
    int happiness;
    MyDesktop desktop = new MyDesktop();
    desktop.apply(wallpaper);
    happiness = INFINITY;
    return happiness;
}
```

另外一种写法：通过4个空格（即一个Tab/4字节缩进）的形式

效果：
    private static int updateDesktop(Image wallpaper){
        int happiness;
        MyDesktop desktop = new MyDesktop();
        desktop.apply(wallpaper);
        happiness = INFINITY;
        return happiness;
    }

注意一点的是以上两种形式的表现出来的字体大小不一致

## 2.4 行内代码
正文中的代码，则通过输入`` 框出, 起到标记作用
>\`ctrl+a\`

效果：
>这是一段行间插入 `ctrl+a` 的展示语句

## 2.5 列表
使用`·`、`+`、或`-`标记无序列表，如：
> \-（+\*） 第一项
> \-（+\*） 第二项
> \- （+\*）第三项

**注意**：标记后面最少有一个 _斜体_ 或 _制表符_。若不在引用区块中，必须和前方段落之间存在空行。

效果：
> + 第一项
> + 第二项
> + 第三项

有序列表的标记方式是将上述的符号换成数字,并辅以`.`，如：
> 1 . 第一项   
> 2 . 第二项    
> 3 . 第三项    

效果：
> 1. 第一项
> 2. 第二项
> 3. 第三项

## 2.6 加粗和倾斜
在强调内容两侧分别加上`*`或者`_`，前后空格与文本隔开, 如：
> \*斜体\*，\_斜体\_    
> \*\*粗体\*\*，\_\_粗体\_\_

效果：
> *斜体*，_斜体_    
> **粗体**，__粗体__

## 2.7 区块引用
在段落的每行或者只在第一行使用符号`>`,还可使用多个嵌套引用，如：
> \> 区块引用  
> \>> 嵌套引用  

效果：
> 区块引用  
> 区块引用  
>> 嵌套引用\
>> 嵌套引用

注意：可以使用 `\` 换行

## 2.8 分割线
分割线最常使用就是三个或以上`*`，还可以使用`-`和`_`。 如：
> \***
> \---
> \___

效果:
***

## 2.9 链接
链接可以由两种形式生成：**行内式**和**参考式**。    
**行内式**：
> \[Anti的Markdown库\]\(https:://github.com/Anti/Markdown "Markdown"\)

效果：
> [Anti的Markdown库](https:://github.com/Anti/Markdown "Markdown")

**参考式**：
> \[Anti的Markdown库1\]\[1\]    
> \[Anti的Markdown库2\]\[2\]    
> \[1\]:https:://github.com/Anti/Markdown "Markdown"    
> \[2\]:https:://github.com/Anti/Markdown "Markdown"   


效果：
> [Anti的Markdown库1][1]    
> [Anti的Markdown库2][2]

[1]: https:://github.com/Anti/Markdown "Markdown"
[2]: https:://github.com/Anti/Markdown "Markdown"

**注意**：上述的`[1]:https:://github.com/Anti/Markdown "Markdown"`不出现在区块中。

## 2.10 图片
添加图片的形式和链接相似，只需在链接的基础上前方加一个`！`。

效果：
>![Anti](https://avatars2.githubusercontent.com/u/47650225?s=460&u=00beab3c9945d3c86cfc805393acdd5f0927ca6e&v=4)

## 2.11 反斜杠`\`
相当于**反转义**作用。使符号成为普通符号。

## 2.11 表格
列表的使用(非traditonal markdown)：

用`|`表示表格纵向边界，表头和表内容用`-`隔开，并可用`:`进行对齐设置，两边都有`:`则表示居中，若不加`:`则默认左对齐。

|代码库       |链接  |
|:----------:|------|
|MarkDown    |[https://github.com/Anti/Markdown](https://github.com/Anti/Markdown "Markdown")|
|MarkDownCopy|[https://github.com/Anti/Markdown](https://github.com/Anti/Markdown "Markdown")|

## 小结
>相信聪明的同学已经知道我为什么建议一开始用vscode写markdown了——原因很简单，分栏输入和预览，你可以直观的看到自己输入的代码渲染后的效果，当然，这其实是大部分markdown编辑器都支持的行为——typora有些不太一样，它不是这种分栏模式。

>如果你是印象笔记或者有道云笔记的用户，其实这两个笔记现在也都支持markdown了，但是说实话，使用体验我个人认为并不好，而且最重要的是，抹杀了markdown的自由性，既然都用笔记了，好像用不用markdown也无所谓了。

>markdown的语法并不多，也没有很复杂的格式，样式完全基于软件所支持的CSS样式渲染，很多时候，简单的就是最好的。你不太可能拿markdown来写一篇正式的论文，但是作为日常的笔记来说，markdown再好不过——够用、可迁移、专注写作。

>windows上的markdown编辑神器——typora。用熟了markdown的语法后，你可以立即抛弃vscode，投身typora的怀抱。

## 尝试一下
+ **Chrome**下的插件诸如`stackedit`与`markdown-here`等非常方便，也不用担心平台受限。
+ **在线**的dillinger.io评价也不错。  
+ **Windowns**上的markdown编辑神器——typora。    
+ **Mac**下的Mou是国人贡献的，口碑很好。
+ **Linux**下的ReText不错。    

**当然，最终境界永远都是笔下是语法，心中格式化 :)。**

****
**注意**：不同的Markdown解释器或工具对相应语法（扩展语法）的解释效果不尽相同，具体可参见工具的使用说明。
虽然有人想出面搞一个所谓的标准化的Markdown，[没想到还惹怒了健在的创始人John Gruber]
(http://blog.codinghorror.com/standard-markdown-is-now-common-markdown/ )。
****
以上基本是所有traditonal markdown的语法。