# 介绍一下CSS的盒子模型？
  有两种， IE 盒子模型、标准 W3C 盒子模型；
  1) IE的content部分包含了 border 和 pading;
  2）W3C的盒模型： 内容(content)、填充(padding)、边界(margin)、 边框(border).
  
# CSS 选择符有哪些？ 
  1.id选择器（ # myid）
  2.类选择器（.myclassname）
  3.标签选择器（div, h1, p）
  4.相邻选择器（h1 + p）
  5.子选择器（ul > li）
  6.后代选择器（li a）
  7.通配符选择器（ * ）
  8.属性选择器（a[rel = "external"]）
  9.伪类选择器（a: hover, li: nth - child）
  
# CSS 优先级算法如何计算？
  优先级为:
  !important >  id > class > tag
  important 比 内联优先级高
  
# css定义的权重
  /*权重为1*/
  div{
  }
  /*权重为10*/
  .class1{
  }
  /*权重为100*/
  #id1{
  }
  /*权重为100+1=101*/
  #id1 div{
  }
  /*权重为10+1=11*/
  .class1 div{
  }
  /*权重为10+10+1=21*/
  .class1 .class2 div{
  }
  如果权重相同，则最后定义的样式会起作用，但是应该避免这种情况出现

# 如何居中div？
  div{
    width:200px;
    margin:0 auto;
  }

# 居中一个浮动元素
  .div {
  Width:500px ; height:300px;//高度可以不设
  Margin: -150px 0 0 -250px;
  position:relative;相对定位
  background-color:pink;//方便看效果
  left:50%;
  top:50%;
  }
  
# 解释下浮动和它的工作原理。
  关于浮动我们需要了解，浮动的框可以向左或向右移动，直到它的外边缘碰到包含框或另一个浮动框的边框为止。
  要想使元素浮动，必须为元素设置一个宽度（width）。虽然浮动元素不是文档流之中，但是它浮动后所处的位置依然是在浮动之前的水平方向上。
  由于浮动框不在文档的普通流中，所以文档的普通流中的块框表现得就像浮动框不存在一样，下面的元素填补原来的位置。
  有些元素会在浮动元素的下方，但是这些元素的内容并不一定会被浮动的元素所遮盖，对内联元素进行定位时，这些元素会考虑浮动元素的边界，
  会围绕着浮动元素放置。也可以把浮动元素想象成是被块元素忽略的元素，而内联元素会关注浮动元素的。 
  
# 列举不同的清除浮动的技巧，并指出它们各自适用的使用场景。
  1.使用空标签清除浮动。这种方法是在所有浮动标签后面添加一个空标签定义css clear:both.弊端就是增加了无意义标签。
  2.使用overflow。给包含浮动元素的父标签添加css属性overflow:auto;zoom:1;zoom:1用于兼容IE6。
  3.使用after伪对象清除浮动。该方法只适用于非IE浏览器。使用中需注意以下几点。
    一、该方法中必须为需要清除浮动元素的伪对象中设置height:0，否则该元素会比实际高出若干像素；
    二、content属性是必须的，但其值可以为空，content属性的值设为”.”，空亦是可以的。
  此三种方法各有利弊，使用时应择优选择，比较之下第二种方法更为可取。
  
# 列出display的值，说明他们的作用。position的值， relative和absolute定位原点是？
  1.
  block 象块类型元素一样显示。
  none 缺省值。象行内元素类型一样显示。
  inline-block 象行内元素一样显示，但其内容象块类型元素一样显示。
  list-item 象块类型元素一样显示，并添加样式列表标记。
   
  2.
  *absolute
        生成绝对定位的元素，相对于 static 定位以外的第一个父元素进行定位。
   
  *fixed （老IE不支持）
        生成绝对定位的元素，相对于浏览器窗口进行定位。
   
  *relative
        生成相对定位的元素，相对于其正常位置进行定位。
        
# 为什么要初始化CSS样式？
  因为浏览器的兼容问题，不同浏览器对有些标签的默认值是不同的，如果没对CSS初始化往往会出现浏览器之间的页面显示差异。
  当然，初始化样式会对SEO有一定的影响，但鱼和熊掌不可兼得，但力求影响最小的情况下初始化。
  最简单的初始化方法就是： {padding: 0; margin: 0;} （不建议）
  淘宝的样式初始化：
  body, h1, h2, h3, h4, h5, h6, hr, p, blockquote, dl, dt, dd, ul, ol, li, pre, form, fieldset, legend, button, input, textarea, th, td { margin:0; padding:0; }
  body, button, input, select, textarea { font:12px/1.5tahoma, arial, \5b8b\4f53; }
  h1, h2, h3, h4, h5, h6{ font-size:100%; }
  address, cite, dfn, em, var { font-style:normal; }
  code, kbd, pre, samp { font-family:couriernew, courier, monospace; }
  small{ font-size:12px; }
  ul, ol { list-style:none; }
  { text-decoration:none; }
  a:hover { text-decoration:underline; }
  sup { vertical-align:text-top; }
  sub{ vertical-align:text-bottom; }
  legend { color:#000; }
  fieldset, img { border:0; }
  button, input, select, textarea { font-size:100%; }
  table { border-collapse:collapse; border-spacing:0; }
  
# 如何优化网页的打印样式？
  <link rel = "stylesheet" type = "text/css" media = "screen" href = "xxx.css"/>
  其中media指定的属性就是设备，显示器上就是screen，打印机则是print，电视是tv，投影仪是projection。打印样式示例如下：
  
  <link rel = "stylesheet" type = "text/css" media = "print" href = "yyy.css"/>
  但打印样式表也应注意以下事项：
  
  打印样式表中最好不要用背景图片，因为打印机不能打印CSS中的背景。如要显示图片，请使用html插入到页面中。
  最好不要使用像素作为单位，因为打印样式表要打印出来的会是实物，所以建议使用pt和cm。
  隐藏掉不必要的内容。（@print div{display:none;}）
  打印样式表中最好少用浮动属性，因为它们会消失。如果想要知道打印样式表的效果如何，直接在浏览器上选择打印预览就可以了。
  
# 在书写高效CSS时会有哪些问题需要考虑？
  1.样式是：从右向左的解析一个选择器；
  2.ID最快，Universal最慢有四种类型的key selector，解析速度由快到慢依次是：ID、class、tag和universal ；
  3.不要tag-qualify（永远不要这样做ul#main-navigation{}ID已经是唯一的，不需要Tag来标识，这样做会让选择器变慢。）；
  4.后代选择器最糟糕（换句话说，下面这个选择器是很低效的：html body ul li a{}）；
  5.想清楚你为什么这样写；
  6.CSS3的效率问题（CSS3选择器（比如:nth-child）能够漂亮的定位我们想要的元素，又能保证我们的CSS整洁易读。但是这些神奇的选择器会浪费很多的浏览器资源。）；
  7.我们知道#ID速度是最快的，那么我们都用ID，是不是很快。但是我们不应该为了效率而牺牲可读性和可维护性。
  
