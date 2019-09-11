# HTML-CSS-JS-study
HTML&CSS学习笔记
                                                                                                                                     作者:YMYGABE


包裹文字便签
html 


表示文档头部
head


表示网页标题
title


表示所有网页内容放在body中
body


表示一个容器或者盒子
div


和div的功能类似，span可以来装小段文字和div的区别就是在一行内显示
span


表示标题 数字越大 文字越小
h1和h6


表示段落标签
<p> </p>


表示一条水平分割线
<hr></hr>


表示无序列表
<ul><li> </li></ul>              /*list-style:none 可以消除li的小点点*/

    

表示斜体
<i></i>   <em></em>


 表示加粗
<strong></strong>


表示换行
<br></br> 


img图片
alt属性 当图片没有办法显示时用来提示
title属性 当鼠标移动到图片的时候，用来提示用户的文字
<img src="../img/baidu.png"  alt="这是一个图片" title="图片">

图片路径
./                     表示同级路径
../                    表示上级路径
../../                 表示上上级路径
././                   表示下下级路径


a标签 表示超链接，可以连接一切资源（包括网址视频文字等）
<a href="http://www.baidu.com" target="_blank"></a>
/*href属性：超链接的地址target属性：_blanl 表示新建一个浏览器标签页来显示超链接的内容，不会覆盖原来的网页。*/
<style>
    a{
        text-decoration:none;              /*a标签文字下划线去除：*/
    }
</style>




1.css是什么？
层叠样式表，修饰网页结构
2.如何去使用css？
a.在html网页中，加入一个style标签，在这个style标签里面写css代码
b.可以直接把style里面的代码放到一个单独的文件中，通过link标签去引入
c.直接在html开始标签的style属性里面去写css代码

id选择器
#box{}

应用场景：ID表示唯一，如果说网页中有一个唯一的元素需要修饰，用ID选择器。
类选择器
.box{}

应用场景：去修饰同一类型元素，有多个元素具有同样的样式的时候，可以用类选择器。

标签选择器
p{}   span{}   div{}   h{}


应用场景：可以影响整个网页里面的相同标签的元素。

相邻选择器
  .box+p{}             

 可以选择相邻两个元素、

多元素选择器   
.box1 , .box2 , .box3{}  

 用逗号隔开，可以简化代码，如果三个元素都有相同性质，可以用多元素同时写

后代选择器   
 .box p{}   （中间是空格）

   会将后面的子类孙类等全部选中

子类选择器  
 .box>p{}

只选择子类元素
属性选择器
input[name^=u]{}         (元素[属性=属性值])









border---边框：
boeder-width:4px;          /*边框宽度*/
border-stysle:solid;       /*边框风格  不简便的写法*/

border-color:red;            /*边框颜色  不简便的写法*/
solid 表示实线 dotted表示点线 
dashed表示虚线
<style>
    .box{
         width:100px;
        height:100px;
        border: red solid 1px;
    }
    .box2{
        width:100px;
        height:100px;
        border-radius:10px;      
        /*设置边框边变圆  border-top-right-radius：表示右上的边框半径（以此类推）*/
    }
    /*边框圆角*/；
    border-radius:20px;                    /*同时设置四个角*/
    border-radius:20px，10px;              /*分别设置两个角*/
    border-radius:20px，10px，10px;        /*分别设置三个角*/
    border-radius:20px，20px，10px，10px;  /*分别设置四个角*/

   /*设置圆（前提宽与高一致）*/
    border-radius:50%
</style>




文本相关属性

          
<style>
.text{
text-align:center;               /*文字水平居中*/
}

.text2{
line-height:50pxl;/*文字垂直居中,让line-height等于盒子高度 line-height=height*/
}
text3{
text-indent:50px; /*设置文字的缩进，在用background设置图片的时候可以设置成-999px,使文字隐藏*/
}
text4{
letter-spacing:10px;      /*设置文字间间距，normal时候为默认间距*/
font-size:12px;           /*设置文字大小*/
font-weight:100px;         /*加粗等（bold粗 bolder更粗 light更细）也可用px设置*/
font-famliy: 定义字体 “”+serif;  /*字体样式*/
}
</style>




margin&padding

margin需要注意的问题：
body有默认的margin ,所以一般都会先来一个这个
body{
    margin:0px;
}


如果设置了上下两个盒子的margin 两个盒子的距离是以最大的那个margin为准。
盒子居中：
margin:10px auto;  /*先上下在左右*/

padding：内边距 
作用：用来控制盒子内容的摆放
总结：padding会把盒子整体撑大，padding撑大多少width或者height就减多少
display：inline-block   在一行内显示，（a标签使用可以支持宽高）
text-align：；  水平对齐方式
vertical-align:;  垂直对齐方式 



  
定位---position
position：relative        相对定位
position：absolute        绝对定位




position：fixed          固定定位

          其中left  right  top  bottom  都是定位的，相对于浏览器的可视区域



伪元素
<style>
    /*--在内容之后加入--*/
    a::after{
        content:"搜索一下";
        color:red;
    }
     /*--在内容之后加入--*/
      a::befor{
        content:"noding";
        color:green;
    }
</style>

<body>
    <a href="">
     百度
    </a>
</body>





伪类
a:link{}------a链接没有被访问的时候的状态

a:visited{}----a链接被访问的时候的状态

a:hover{}-----a 链接被鼠标光标选中或是说移动到上面时候的状态

a:active{}----a链接被点击但是鼠标未放开的时候的状态

其他的元素都可以用，触类旁通就行了






background
background:url(../img/baidu-all.png) no-repeat;  /*设置背景图片----好处：可以节约服务器*/
background-position:0px 0px;            /*对背景图片的具体定位*/

background-repeat:no-repeat;           /*不重复*/
background-repeat:repeat-x;            /*横向重复*/

background-color:red;                  /*背景颜色*/



nth-of-type(){}运用



根据我的个人理解，就是控制名为search的div中的li中的第几个a-------以此类推（还有其他的nth,后期进行补充）

table-----表格
<body>
    <table>
            /*第一行*/
        <tr>
            <td>第一行第一列</td>
            <td>第一行第二列</td>
            <td>第一行第三列</td>
        </tr>
        /*第二行*/
        <tr>
            <td>第二行第一列</td>
            <td>第二行第二列</td>
            <td>第二行第三列</td>
        </tr>
    </table>
</body>

css的一些属性：可以更改样式


效果：

合并单元格
        水平合并
<table>
            /*第一行*/
        <tr >
            <td colspan="3" align="center">第一行第一列</td> /*第一行第一列与后面的合并*/
            <td>第一行第二列</td>
            <td>第一行第三列</td>
        </tr>
        /*第二行*/
        <tr>
            <td>第二行第一列</td>
            <td>第二行第二列</td>
            <td>第二行第三列</td>
        </tr>
    </table>



             
         垂直合并
<body>
    <table>
            /*第一行*/
        <tr>
            <td rowspan="3">第一行第一列</td>    /*垂直合并单元格*/
            <td>第一行第二列</td>
            <td>第一行第三列</td>
        </tr>
        /*第二行*/
        <tr>
            <td>第二行第一列</td>
            <td>第二行第二列</td>
            <td>第二行第三列</td>
        </tr>
    </table>
</body>







form----表单
一定要加name属性，不然无法传输数据（需要传输数据的）
<form action="www.baidu.com" method="">            /*action就是要传输信息的网站  method就是传输方式*/
    <input type="text" name="username"/></br>     /*text可以理解为账号,加br可以换行*/
    <input type="password" name="userpss"/></br>           /*password就是密码，用户输入的时候会变成****/
    <input type="submit"  value="登录"/>            
</form>




input的标签
type="text"            表示文本输入框，用来输入文本（账号，用户名，手机号等）
type="psaaword"        表示密码，用户输入不可见
type="checkbox"        复选框（多选）
type="radio"           单选框 注意：要单选先加 相同 name属性
type="hidden"          隐藏域 数据用户看不见
type="button"          普通按钮 点击后不会发生提交，一般用来后期加js使用
type="submit"          提交按钮 点击后提交信息
type="file"            文件上传按钮  作用：可以让你选择需要上传的文件

input的其他属性
<input type="text" value="请输入用户名"/>

能看到，也可以进行修改以及输入


--------------------------------------------------------------------------------
<input type="text" value="请输入用户名" readonly />

只能看，啥也不能做，无法输入无法删除，可以传输数据


--------------------------------------------------------------------------------
<input type="text" value="请输入用户名" diabled/>

颜色变灰，同样只能看，算是被禁用，无法传输数据


--------------------------------------------------------------------------------
<input type="checkbox" checked/>
<input type="radio" checked/>

被选中状态

文本域---textarea
    <textarea rows="" cols="" name="">      /* 加入name才可以传输数据  rows设置高 cols设置宽*/
    
    </textarea>




按钮-----button

<button type="button">登录<img src="../img/a1.png" ></button>   /*可以插入图片，功能强*/





下拉选择框---select
	<select name="city" size="4" multiple>
				<option value="">北京</option>
				<option value ="">上海</option>
				<option value ="">广州</option>
				<option value ="">深圳</option>
				<option value ="">福建</option>
    </select>







label
<label for="man">男</label><input type="radio" name="sex" id="man" value="" />
<label for="woman">女</label><input type="radio" name="sex" id="woman" value="" />


效果就是点男的或者女两个字也可以选择
或者直接把input放在label里，但是不要加for=""  不然可能会出问题
<label>haha<input type="radio" name="" id="" value=""/></label>
