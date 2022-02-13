# 字符串
字符串是一个可变的字符列表。支持所有以 unicode 编码的字符。

要声明文字，请将文本括在两个双引号 ("") 中。
```c
"你好，世界"
```

## 转义
大多数其他编程语言使用反斜杠 (\) 后跟一个字母或数字组合来声明转义序列。但是，由于标准拼音键盘上没有现成的反斜杠，气使用中间点 (·) 代替反斜杠。
支持少数转义字符：
```c
"·"" // 一个双引号字符。
"··" // 中间点。
"·a" // 警报声。
"·b" // 退格。
"·f" // 换页。
"·n" // 换行符。
"·r" // 回车。
"·t" // 选项卡。
"·v" // 垂直制表符。
```
> 有关转义序列的更多信息，请参考 [这篇文章]( https://en.wikipedia.org/wiki/Escape_sequences_in_C )。

##静态方法

#### **字符串。串到数**（字符串）
将给定字符串转换为数字。
```c
系统。打印行（字符串。串到数（"1"）+ 1） // 2
```

##方法

#### **长度**（）
返回字符串的长度。
```c
变量 符串 = "你好"
系统。打印行（符串。长度（））  // 2
```
#### **大写**（）
返回一个字符串，其中所有字符都为大写。
```c
变量 符串 = "test"
系统。打印行（符串。长度（））  // TEST
```
#### **小写**（）
返回一个字符串，其中所有字符都是小写。
```c
变量 符串 = "TEST"
系统。打印行（符串。长度（））  // test
```
#### **子串**（数字）
返回字符串的起始索引和字符串结尾之间的一部分。
```c
变量 符串 = "零一二三"
系统。打印行（符串。子串（1））  // 一二三
```
#### **子串**（数字, 数字）
返回起始索引和结束索引之间的字符串的一部分。
```c
变量 符串 = "零一二三"
系统。打印行（符串。子串（1，3））  // 一二
```
#### **指数**（字符串）
返回与输入字符串匹配的第一个字符的索引。
```c
变量 str = "零一二三"
系统。打印行（str。指数（"二三"））  // 2
```
#### **计数**（字符串）
返回找到输入字符串的次数。
```c
变量 str = "零一二三二一零一二三一二一二"
系统。打印行（str。计数（"一二"））  // 4
```
#### **拆分**（字符串）
按给定的分隔符拆分字符串，并将子字符串存储在列表中。
```c
变量 str = "零一二三二一零一二三一二一二"
系统。打印行（str。拆分（"一"））  // 【零，二三二，零，二三，二，二】
```
#### **替换**（字符串，字符串）
返回一个字符串，其中所有出现的第一个参数都替换为第二个参数。
```c
变量 str = "零一二三二一零一二三一二一二"
系统。打印行（str。替换（"一"，"四五"））  // 零四五二三二四五零四五二三四五二四五二
```
#### **修剪**（）
返回一个从输入字符串的开头和结尾删除了空格的字符串。
```c
变量 str = "·t·n  四是四  ·n·t"
系统。打印行（str。修剪（））  // 四是四
```
#### **修剪**（字符串）
返回一个新字符串，并从输入字符串的开头和结尾删除参数的字符。
```c
变量 str = "abbaba四是四babaab"
系统。打印行（str。修剪（"ab"））  // 四是四
```
#### **修剪始**（）
返回一个从输入字符串开头删除空白的字符串。
```c
变量 str = "·t·n  四是四  ·n·t"
系统。打印行（str。修剪始（））  // 四是四  ·n·t
```
#### **修剪始**（字符串）
返回一个新字符串，其中参数的字符从输入字符串的开头删除。
```c
变量 str = "abbaba四是四babaab"
系统。打印行（str。修剪始（"ab"））  // abbaba四是四
```
#### **修剪端**（）
返回一个从输入字符串末尾删除空白的字符串。
```c
变量 str = "·t·n  四是四  ·n·t"
系统。打印行（str。修剪端（））  // ·t·n  四是四
```
#### **修剪端**（字符串）
返回一个新字符串，其中参数的字符从输入字符串的末尾删除。
```c
变量 str = "abbaba四是四babaab"
系统。打印行（str。修剪端（"ab"））  // 四是四babaab
```