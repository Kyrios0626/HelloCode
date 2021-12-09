# MarkDown 操作手册

## 1.转义字符
要显示原义字符，否则将用于设置Markdown文档中的文本格式\，请在字符前面添加反斜杠（）。

\* Without the backslash, this would be a bullet in an unordered list.


## 2.标题
\# 一级标题  
\#\# 二级标题  
\#\#\# 三级标题  
\#\#\#\# 四级标题  
\#\#\#\#\# 五级标题  
\#\#\#\#\#\# 六级标题  

## 3.段落
用空行来表示段落

    I really like using Markdown.

    I think I'll use it to format all of my documents from now on.
    
## 4.换行
在每行最后加两个空格一个enter,实现换行

    This is the first line.  
    And this is the second line.

## 5.着重
#### 粗体
```
I just love **bold text**. 
I just love __bold text__. 
```
I just love **bold text**.  
I just love __bold text__. 

#### 斜体
```
Italicized text is the *cat's meow*.  
Italicized text is the _cat's meow_. 
```
Italicized text is the *cat's meow*.  
Italicized text is the _cat's meow_. 

#### 粗斜体文本
```
This text is ***really important***.   
This text is ___really important___.  
```
This text is ***really important***.   
This text is ___really important___.  

#### 删除线
```
~~The world is flat.~~ We now know that the world is round. 
```
~~The world is flat.~~ We now know that the world is round. 

#### 下划线
```
++这句话有下划线++. 
```
++这句话有下划线++. 

#### 块引用
要创建blockquote，请在段落前面添加一个> 。

块引用可以包含多个段落。> 在段落之间的空白行上添加一个。

块引用可以嵌套。>> 在要嵌套的段落前面添加一个。

```
> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.  
```

> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.  
 
块引用可以包含其他Markdown格式的元素。并非所有元素都可以使用-您需要进行实验以查看哪些元素有效。
```
> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.  
```

> #### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
>  *Everything* is going according to **plan**.  

## 6.清单
#### 有序列表
要创建有序列表，请在订单项中添加数字和句点。数字不必按数字顺序排列，但列表应以数字开头。  
```
1. First item
2. Second item
8. Third item
    1. Indented item
    2. Indented item
1. Fourth item 
```

1. First item
2. Second item
8. Third item
    1. Indented item
    2. Indented item
1. Fourth item  

#### 无序列表
要创建无序列表，请在订单项前添加破折号（-），星号（*）或加号（+）。缩进一个或多个项目以创建嵌套列表。 
```
- First item
- Second item
- Third item
    - Indented item
    - Indented item
- Fourth item  
```

- First item
- Second item
- Third item
    - Indented item
    - Indented item
- Fourth item  

> 不同标识不能一起用 行间距很大 
```
> + First item
> * Second item
> - Third item
> - Fourth item 
```
> + First item
> * Second item
> - Third item
> - Fourth item 

#### 在列表中添加元素
要在保留列表连续性的同时在列表中添加另一个元素，请**将该元素缩进四个空格或一个制表符**，如以下示例所示。  
*  This is the first list item.
*  Here's the second list item.

    I need to add another paragraph below the second list item.

*  And here's the third list item.  

插入的元素可以是 **段落,块引用,代码块,图片**

#### 任务清单
要创建任务列表，请在任务列表项之前添加破折号（-）和方括号，并[ ]在其前面加上一个空格（）。要选择一个复选框，请在方括号（[x]）之间添加x 。
```
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
```

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media

## 7.代码
要将单词或短语表示为代码，请将其括在勾号``中 
```
At the command prompt, type `nano`.
```

At the command prompt, type `nano`.

#### 转义刻度线
如果要表示为代码的单词或短语包含一个或多个刻度线，可以通过将单词或短语括在双刻度线（``）中来对其进行转义。
```
前面有字``Use `code` in your Markdown file.``后面也有字
```

前面有字``Use `code` in your Markdown file.``后面也有字

#### 代码块
要创建代码块，请在代码块的每一行缩进至少四个空格或一个制表符。

    <html>
      <head>
      </head>
    </html>
    
#### 围栏代码块
根据Markdown处理器或编辑器的不同，您将在代码块之前和之后的行上使用三个刻度线（```）或三个波浪号（~~~）。最好的部分:您不必缩进任何行！
>  \`\`\`
> {  
>   "firstName": "John",  
>   "lastName": "Smith",  
>   "age": 25  
> }  
> \`\`\`

```
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

## 8.水平线
要创建水平线***，请单独在一行上使用三个或更多的星号（），破折号（---）或下划线（___）。
```
***
---
_________________
```

***
---
_________________

## 9.链接
要创建链接，请将链接文本括在方括号（例如[百度]）中，然后立即在URL后面加上括号（例如(https://www.baidu.com/)）中的URL 。  
```
My favorite search engine is [这个地方点了就去百度了](https://www.baidu.com/).
```
My favorite search engine is [这个地方点了就去百度了](https://www.baidu.com/).

#### 为链接添加标题
您可以选择为链接添加标题。当用户将鼠标悬停在链接上时，这将显示为工具提示。要添加标题，请将其括在URL后面的括号中。
```
My favorite search engine is [悬停在我这](https://www.baidu.com/ "然后你就能看到这句话").
```

My favorite search engine is [悬停在我这](https://www.baidu.com/ "然后你就能看到这句话").

#### 网址和电子邮件地址
要将URL或电子邮件地址快速转换为链接，请将其括在尖括号中  
```
<https://markdown.p2hp.com>  
<fake@example.com>
```

<https://markdown.p2hp.com>  
<fake@example.com>

#### 格式化链接
为了强调链接，请在方括号和括号之前和之后添加星号。
```
I love supporting the **[EFF](https://eff.org)**.  
This is the *[Markdown Guide](https://markdown.p2hp.com)*.
```

I love supporting the **[EFF](https://eff.org)**.  
This is the *[Markdown Guide](https://markdown.p2hp.com)*.

#### 参考样式链接
参考样式链接是一种特殊的链接，它使URL在Markdown编写中更易于显示和阅读。引用样式的链接分为两部分：与文本保持内联的部分,以及在文件中其他位置存储的部分，以使文本易于阅读。
```
it was a [编写时,这样你就能通读这一句话了][1], and that means comfort.

[1]: <https://www.baidu.com/> "我是链接标题,点我去百度啊"
```

it was a [编写时,这样你就能通读这一句话了][1], and that means comfort.

[1]: <https://www.baidu.com/> "我是链接标题,点我去百度啊"

#### 图片
要添加图像，请添加感叹号（!），然后在括号中添加替代文本，并在括号中添加图像资源的路径或URL。您可以选择在括号中的URL之后添加标题  

```
前面有字![这里面的字不显示](https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fup.enterdesk.com%2Fedpic_source%2Fe6%2F7b%2F28%2Fe67b281611091c5a9dbbb52e586ed92a.jpg&refer=http%3A%2F%2Fup.enterdesk.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1641543266&t=1a1bd49613dcd4a6247b4045acaf21e4 "这里显示的是标题 或者说是注释")后面也有字
```

前面有字![这里面的字不显示](https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fup.enterdesk.com%2Fedpic_source%2Fe6%2F7b%2F28%2Fe67b281611091c5a9dbbb52e586ed92a.jpg&refer=http%3A%2F%2Fup.enterdesk.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1641543266&t=1a1bd49613dcd4a6247b4045acaf21e4 "这里显示的是标题 或者说是注释")后面也有字

#### 链接图像
要向图像添加链接，请将图像的Markdown括在方括号中，然后在括号中添加链接  
这样点击图片就能跳转了

```
[![这里面的字不显示,第一个图片会显示在md文件上](https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fup.enterdesk.com%2Fedpic_source%2Fe6%2F7b%2F28%2Fe67b281611091c5a9dbbb52e586ed92a.jpg&refer=http%3A%2F%2Fup.enterdesk.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1641543266&t=1a1bd49613dcd4a6247b4045acaf21e4 "点我跳转到链接地址,")](https://www.baidu.com/)
```


[![这里面的字不显示,第一个图片会显示在md文件上](https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fup.enterdesk.com%2Fedpic_source%2Fe6%2F7b%2F28%2Fe67b281611091c5a9dbbb52e586ed92a.jpg&refer=http%3A%2F%2Fup.enterdesk.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1641543266&t=1a1bd49613dcd4a6247b4045acaf21e4 "点我跳转到后面的链接地址,")](https://www.baidu.com/)

#### 禁用自动URL链接

将URL表示为带有刻度线的代码来删除该链接。  
```
`http://www.example.com`
```

`http://www.example.com`


## 10.表格
要添加表，请使用三个或多个连字符（---）创建每列的标题，并使用管道（|）分隔每列。您可以选择在表的任一端添加管道。
```
| Syntax | Description |
| --- | ----------- |
| Header | Title |
| Paragraph | Text |
```


| Syntax | Description |
| --- | ----------- |
| Header | Title |
| Paragraph | Text |

#### 对齐
您可以通过:在标题行内的连字符的左侧，右侧或两侧添加一个冒号（），以使列中的文本左，右或居中对齐。  
```
| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |
```


| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |

## 11.脚注
要创建脚注参考，请在方括号（\[\^1\]）内添加插入符号和标识符。标识符可以是数字或文字，但他们不能包含空格或制表符。标识符仅将脚注参考与脚注本身相关联-在输出中，脚注按顺序编号。

在括号内使用另一个插入符号和数字添加脚注，并用冒号和文本（\[\^1\]: My footnote.）括起来。您不必在文档末尾添加脚注。你可以把他们的任何地方，除了像列表一样，块报价，和表格等元素里面。  

```
例子:Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.
[^bignote]:这是一个包含多个段落和代码的代码  
    缩进段落以将其包括在脚注中。  
    { my code }  
    添加任意多的段落。
```    

例子:Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.
[^bignote]:这是一个包含多个段落和代码的代码  
    缩进段落以将其包括在脚注中。  
    { my code }  
    添加任意多的段落。