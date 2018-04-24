# 20180423
*函数可以存到变量中。
var a = function(){
	alert("a");
};
    a();	

*cssText  
el.style.cssText="width:200px;height:200px"; 直接设置会把之前的行间样式覆盖掉；
el.style.cssText+="width:200px;height:200px"; 只修改当前改写的样式； 

*属性操作的第二种写法
<body>
<div>
    <select>
        <option>width</option>
        <option>height</option>
        <option>background</option>
    </select>
    <input type="text" name="" value=""/>
    <input class="btn" type="button" value="设置"/>
    <div class="box"></div>
</div>
<script>
    var select=document.querySelector("select");
    var inp=document.querySelector("input");
    var box=document.querySelector(".box");
    var btn=document.querySelector(".btn");
    /*
     var sel=select.value;  写在事件外面的话，代码在执行之前值就会被清空，所以代码不执行
     var val=inp.value;
   */
    btn.onclick=function(){
        var sel=select.value;
        var val=inp.value;
        box.style[sel]=val;
    };
    /*
     使用 . 操作属性时，属性名不能用变量
     如果 属性名 是一个变量调用 请用 第二种写法 []

     [] 属性操作第二种写法，在[] 接收是个字符串
     */
</script>
</body>

*classList
<div id="box" class="box2 box3 box4"></div>
<script type="text/javascript">
var box = document.querySelector('#box');
console.log(box.classList[2]);
</script>

length属性

box.classList.add（） //向元素中添加class，每个class之间以, 号隔开
box.classList.remove（） //删除元素中的某个class
box.classList.toggle()   //切换 如果是一个已有的 class 就删除，如果是新的class 就添加
box.classList.contains()//contains 判断是否有这个class, 当元素中有这个class 就返回true，否则返回false

*模拟复选框
<style type="text/css">
		#box {
			margin: 100px auto; 
			width: 20px;
			height: 20px;
			border: 1px solid #000;
			padding: 4px;
			background-clip: content-box;
		}
		.checked {
			background: #000;
		}
   </style>
</head>
<body>
<div id="box" class="checked"></div>
<script type="text/javascript">
var box = document.querySelector('#box');
box.onclick = function(){
	box.classList.toggle("checked")
};
</script>
</body>

*js的程序执行顺序
从上到下，从左到右

*
