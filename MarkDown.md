# Markdown
Practice on Markdown knowlodge

<http://www.markdown.cn/>  
<http://www.jianshu.com/p/q81RER> 简书  
***
# **标题**

Markdown 支持两种标题的语法，类 Setext 和类 atx 形式。

类 Setext 形式是用底线的形式，利用 = （最高阶标题）和 - （第二阶标题），例如：

一级标题
===========
二级标题
-----------

> ` 一级标题 `  
> ` =========== `  
> ` 二级标题 `   
> ` ----------- `  

类 Atx 形式则是在行首插入 1 到 6 个 # ，对应到标题 1 到 6 阶，例如：

# 一级标题
## 二级标题
### 三级标题

Code: 
> ` # 一级标题 `  
> ` ## 二级标题 `  
> ` ### 三级标题 `  

Note: 总共六级标题
 ***

# **列表**

#### 无序列表
无序列表使用星号、加号或是减号作为列表标记：
* 1
  - 1
  + 2
  
Code: 
> ` * 1 ` <br>  ` - 1 ` <br>  ` + 2 `

#### 有序列表
有序列表则使用数字接着一个英文句点：
Note: 可以完全不用在意数字的正确性。
1. a
6. b
3. c

Code: 
> ` 1. a `  
> ` 6. b `  
> ` 3. c `  

***

# **图片与链接**
图片与链接的差别为：一个惊叹号` ! `
支持两种形式的语法： 行内式和参考式两种形式

### 行内式：
图片为：` ![](){ImgCap}{/ImgCap} `  
链接为：` []() `

Example:
#### 链接
[Bing](http://www.bing.com)

#### 图片
![Moon](http://solarsystem.nasa.gov/docs/moon_and_earth_lroearthrise_frame.jpg)

### 参考式：  
#### 链接
引用：` [Example] [id] `  
定义：` [id]: http://example.com/  "Optional Title Here" `  

Example:
I get 10 times more traffic from [Google] [1] than from
[Yahoo] [2] or [MSN] [3].

  [1]: http://google.com/        "Google"
  [2]: http://search.yahoo.com/  "Yahoo Search"
  [3]: http://search.msn.com/    "MSN Search"

#### 隐式链接
隐式链接标记功能让你可以省略指定链接标记，这种情形下，链接标记会视为等同于链接文字  
引用：` [Google][] `  
定义：` [Google]: http://www.google.com/  "Optional Title Here" ` 

#### 自动链接
比较简短的自动链接形式来处理网址和电子邮件信箱，只要是用尖括号包起来  

<http://www.bing.com/>  

Code:  

> ` <http://www.bing.com/> `

***

# **表格**

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

Code:
> ` | Tables        | Are           | Cool  | `  
> ` | ------------- |:-------------:| -----:| `  
> ` | col 3 is      | right-aligned | $1600 | `  
> ` | col 2 is      | centered      |   $12 | `  
> ` | zebra stripes | are neat      |    $1 | `  

***

# **换行**

* 需要在结尾加两个空格后回车才能启用新行
* 换行的时候手打 ` <br> `

a<br>b

Code:
> ` a<br>b `

***

# **特殊字符自动转换**

在 HTML 文件中,有两个字符需要特殊处理: ` < ` 和 ` & `, 如果你只是想要显示这些字符的原型, 你必须要使用实体的形式 ` &lt; ` 和 ` &amp; `

AT&amp;T 

  > ` AT&amp;T `  
  
4 < 5  

  > ` 4 &lt; 5 `  
  
***

