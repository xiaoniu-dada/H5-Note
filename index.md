# HTML文件部分
1.在 hand 标签内插入手机端适配，快捷键 metav；
2.在 hand 标签内链接 style.css 文件，快捷键 lin；
3.在 hand 标签内链接 anim.css 文件，快捷键 lin；
4.修改 title 标签的内容；
头部
~~~HTML
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
    <link rel="stylesheet" type="text/css" href="css/style.css" />
    <link rel="stylesheet" type="text/css" href="css/anim.css"/>
    <title>项目主题</title>
</head>
~~~
内容部分
~~~HTML
<body>
    <audio src="" class="audio" loop="loop">当前浏览器不支持audio</audio>
   <div id="warp">
			<section class="Pg" style="display: ;">
				<p>LOADING<span class="loading"></span></p>
				<p><span class="number"></span>%</p>
			</section>
			<section class="Pg" style="display: none ;">
				<div class=""></div>
			</section>
			<section class="Pg" style="display: none ;">
			</section>
		</div>
    <script src="js/main.js" type="text/javascript" charset="utf-8" defer="defer"></script>
</body>
~~~
Css部分：
1.清除CSS默认样式
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
2.设置 html，body，#wrap，.Pg 宽高为整个可显示区域，并且内容不可选择，溢出部分隐藏
html,body,#warp,.Pg{
	height: 100%;
	width: 100%;
	overflow: hidden;
    user-select: none;
}
3.设置 #wrap 基于自己相对定位
#wrap {
    position: relative;
}
4.设置 .Pg 背景缩放，绝对定位
.Pg{
	background-size: 100% 100%;
	position: absolute;
}
5.设置.Pg div里面的不给重复，背景缩放
.Pg div{
	background-repeat: no-repeat;
	background-size: 100% 100%;
}
6.单独设置每个 .Pg 1 - #Pn 的背景、层级，背景大小充满；如要过渡动画，为需要过渡的页面添加过渡样式，则添加变形样式，后面使用jJS让其过渡；
.Pg:nth-child(1) {
    background: url();
    z-index: 8;
    /* 无过渡动画则忽略 */
    transition: all 1s; /* 若此页无需过渡则忽略此语句 */
    transform: translate(-100%);
}
/*......*/
#P8 {
    background: url() no-repeat center;
    background-size: 100% 100%;
    z-index: 0;
    /* 无过渡动画则忽略 */
    transition: all 1s;
    transform: translate(-100%);
}
6.使用 子类选择器 设置元素的样式
#P1 > img:nth-child(1) {
    position: absolute;
    left: 0;
    right: 0;
    margin: auto;
    top: 10%;
}
#P1 > img:nth-child(2) {
    position: absolute;
    left: 0;
    right: 0;
    margin: auto;
    top: 20%;
}
/*......*/
7.设置 #music 元素的大小与定位
#music {
    position: absolute;
    width: 20%;
    right: 5%;
    left: 5%;
}
剩下的自由发挥
~~~~~
