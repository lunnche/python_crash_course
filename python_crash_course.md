# Python Crash Course

书的内容：
第一部分：
1 各种数据，将数据存储到列表和字典中的方式。
2 创建数据集合，如何高效遍历这些集合。
3 while循环和if语句检测特定条件，根据是否满足条件执行不同的代码段。这可为自动处理提供极大的帮助
4 获取用户输入，使程序具有交互性，并在用户没停止输入时保持运行状态。
5 编写函数来实现代码段重用。
6 使用类来进一步拓展代码重用，以实现更复杂的行为，从而让简单的程序也能处理复杂情形。
7 编写妥善处理常见错误的程序

学完上述基本概念，就可以编写简短的程序来解决一些明确的问题。
最后，你将向中级编程迈出第一步：学习如何为代码编写测试，以便在进一步改进程序时不用担心可能引入bug。

第二部分：
三个项目：
1 外星人入侵 完成后，你可以开发自己的2d游戏
2 数据可视化 掌握使用通过代码生成的数据集、已经从网络下载下来的数据集、程序自动下载的数据集。 完成后，你将能够编写对大型数据集进行筛选的程序，并以可视化方式将筛选出的数据呈现出来。
3 小型web应用程序“学习笔记”， 这个项目能够让用户将学到的特定主题相关概念记录下来。能够分别记录不同的主题，还可以让其他人建立账户并开始记录自己的学习笔记。 还将学习如何部署项目，让任何人都能够通过网络访问它。


书的相关资源：

https:// nostarch.com/pythoncrashcourse2e/

http://ehmatthes.github.io/pcc_2e/

资源包括：

安装说明
python更新相关
练习答案
备忘单

## 为何使用Python
相较其他语言：

代码行更少
语法有助于创建整洁的代码
更易阅读、调试和扩展

python用途：
编写游戏
创建Web应用
解决商业问题
供各类有趣的公司开发内部工具
在科学领域被大量用于学术研究和应用研究

使用python的一个最重要原因：python社区

编程绝非孤独的修行  programming isn't a solitary pursuit.

大多数程序员都需要向解决过类似问题的人寻求建议，经验最为丰富的程序员也不例外。需要有人帮助解决问题时，有一个联系紧密、互帮互助的社区至关重要。


第一部分各章节内容

chapter1 安装python 运行第一个程序"Hello world!"
chapter2 在变量中存储信息，如何使用文本和数字
chapter3 & chpter4 介绍列表。 列表能够在一个变量中存储任意数量的信息，从而高效地处理数据：只需几行代码，就能够处理数百万个值。
chapter5 if语句
chapter6 字典，字典可以将不同信息关联起来，可在字典中存储任意数量的信息。
chapter7 从用户获取输入，以让程序变成交互式的。while循环。
chapter8 函数
chapter9 类
chapter10 文件，异常
chapter11 为代码编写测试

## chpater 1 getting started
安装python，安装编辑器

python版本

附录A 包含了在各种操作系统下安装python的详细指南

你可能在系统里发现python2，可能是为了支持一些你的系统需要的老版本的程序，你可以保留python2，但你应该使用python3。

python自带了一个在终端窗口中运行的解释器，让你无需保存并运行整个程序就能尝试运行Python代码片段

```
>>> print("hello Python interpreter!")
Hello Python interpreter!
```

三个尖括号意味着输出来自终端会话。

Sublime Text 可以让你在编辑器中运行你的程序而非在终端中。附录B介绍了其他编辑器。

## 文本编辑器和IDE

IDE：integrated development environment

高效的编辑器能干啥：
突出代码结构，让你在编写代码时能够发现常见的bug。
自动缩进
显示代码长度的标志
常见操作快捷键

IDE 是拥有其他一些功能的编辑器，比如：
交互调试器  interactive debuggers
代码自省 code introspection

IDE的一个最常见的例子就是，输入函数名，展示出这个函数有哪些参数。

你知道IDE的这些功能的话，就很好用，如果你是个初学者，这些功能可能让你不知所措。

简单的编辑器，对老旧破电脑更友好，IDE占用资源多。

Sublime Text 设置
1 把Tabs转换为空格
混用tabs和空格，会导致问题，且难于检测，
可以设置成即使你按下tabs键，也默认用空格代替。
View -> Indentation -> Indent Using Spaces   
Tab width 设置成4（个空格）

如果你已经 tabs和空格混用了
View -> Indentation ->Convert Tabs to Spaces

设置line length indicator
python社区的惯例：一行79个字符或更少。
View -> Ruler -> 80

缩进和反缩进代码段
缩进

![image-20220919144133131](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220919144133131.png)

注释掉代码块

![image-20220919144452199](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220919144452199.png)

保存你的配置
上述设置只影响你当前的文件，想让它们适用于Sublime Text打开的所有文件，需要定义你的用户设置。preferences -> Settings 查找文件 preferences.sublime-settings-User.
在文件中输入如下内容：
***
```
{
    "rulers": [80],
    "translate_tabs_to_spaces":true
}
```
***
注意：最后一行后没有逗号，其他都有逗号。

进一步定制：
键盘快捷键：

Every time you use a keyboard shortcut instead of reaching for the mouse or trackpad,you become a bit more efficient.

其他编辑器

IDLE：python附带的文本编辑器，不如Sublime text直观

Geany：一个简单编辑器，可以在编辑器里直接运行程序

Emacs和Vim：受高级程序员青睐，因为手不需要离开键盘

Atom：作为一个编辑器，却有一些IDE才有的功能，集成了git和github，版本管理不用另开终端，Atom还允许安装包

Visual Studio Code：一个像IDE的编辑器，有调试器，版本控制，代码补全功能。

PyCharm：为Python建造的IDE，付费，有免费版PyCharm Community Edition，特点是linter，检查你的代码风格是否与惯例相同，给出格式建议，集成了调试器，有一些模式可以让你高效地使用python库。

Jupyter Notebooks: 科研和聚焦数据的问题用的多，是个网络app，由很多块组成，包括代码块和文本块。文本块适用markdown。jupyter notebook 可以让你不仅仅是在.py文件里写注释，可以写清晰的文本，且可以应用简单的格式。。。每个代码段可独立执行或一起执行，每个代码段有独立的输出区域。
写在一个代码段中的函数是可以被其他代码段调用的，所以notebook太长而你没整明白结构关系的情况下可能会懵。

在macOS上安装Python
一般mac上都装了python，只是可能版本比较旧

检查是否安装了python3
打开终端，输入
```
$ python
```

![image-20220921155303930](https://raw.githubusercontent.com/lunnche/picgo-image/main/image-20220921155303930.png)

按下 ctrl-D 或者 输入exit() 退出python
