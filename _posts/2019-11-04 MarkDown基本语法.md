---
layout:     post
title:      "MarkDown的基本语法"
subtitle:   "介绍博客创建的基本方法和MarkDown的基本语法"
date:       2019-11-04 20:48：52
author:     "Coder-Li-wj"
tags:
    - Life
---
vscode使用Markdown文档编写  
可以新建一个.md文件  
Visual Studio Code 原生就支持高亮Markdown的语法，想要一边编辑一遍预览，有两种方法：  
  1.Ctrl + Shift + P 调出主命令框，输入 Markdown，应该会匹配到几项 Markdown相关命令  
  2.先按Ctrl + K，然后放掉，紧接着再按 v，也能调出实时预览框。【要在英文输入状态下】  

<P style="color:red; font-size:20px; background-color: lightblue; font-weight: 1000">标题</p>
使用 # 号可表示 1-6 级标题，一级标题对应一个 # 号，二级标题对应两个 # 号，以此类推。  

# #一级标题  
## ##二级标题  
### ###三级标题  
#### ####四级标题  
##### #####五级标题  
###### ######六级标题  
  
<P style="color:red; font-size:20px; background-color: lightblue; font-weight: 1000">换行</p>  
 编辑好一行文字后敲两个空行，再按回车键编辑另一行文字  
  
<P style="color:red; font-size:20px; background-color: lightblue; font-weight: 1000">markdown空格缩进以及HTML空格实体</p>  

### 1.markdowm首行缩进方法
> 一个汉字占两个空格大小，所以使用四个空格就可以达到首行缩进两个汉字的效果。有如下几种方法：
>> 1.一个空格大小的表示：<span style="color:red">&ensp</span>;或<span style="color:red">&#8194</span>;，此时只要在相应需要缩进的段落前加上 4个 如上的标记即可，注意要带上分号。  
>> 2.两个空格的大小表示：<span style="color:red">&emsp</span>;或<span style="color:red">&#8195</span>;，同理，使用2个即可缩进2个汉字，推荐使用该方式。  
>> 3.不换行空格：<span style="color:red">&nbsp</sapn>;或<span style="color:red">&#160</sapn>;，使用4个<span style="color:red">&#160</sapn>;即可。  
### 2.HTML中的实体空格  
HTML提供了5种空格实体（space entity），它们拥有不同的宽度，非断行空格<span style="color:red">&nbsp</span>;是常规空格的宽度，可运行于所有主流浏览器。其他几种空格（<span style="color:red">&ensp</span>; <span style="color:red">&emsp</span>; <span style="color:red">&thinsp</sapn>; <span style="color:red">&zwnj</span>; <span style="color:red">&zwj</span></span>;）在不同浏览器中宽度各异。
