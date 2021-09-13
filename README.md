<!--
 * @Author: YinBZ
 * @Date: 2021-09-13 11:26:06
 * @LastEditTime: 2021-09-13 11:49:43
 * @LastEditors: Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \demod:\文件\H5笔记.md
-->
# H5笔记

文件夹路径
~~~
demo
├─index.html
├─css
│ ├─anim.css
│ └─style.css
├─img
│ └─...
├─js
│ └─main.js
└─media
  └─...
~~~
头部
~~~JavaScript
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no" />
    <link rel="stylesheet" type="text/css" href="css/style.css" />
    <link rel="stylesheet" type="text/css" href="css/anim.css"/>
    <title>项目主题</title>
</head>
~~~
内容部分
~~~JavaScript
<body>
    <audio src="">当前浏览器不支持audio</audio>
    <div id="wrap">
        <section class="Pages" id="P1"></section>
        <section class="Pages" id="P2"></section>
        <section class="Pages" id="P3"></section>
    </div>
    <script src="js/main.js" type="text/javascript" charset="utf-8" defer="defer"></script>
</body>
~~~
