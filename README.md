## 简答题
#### 1.行内元素有哪些?块级元素有哪些?
- 常用块级元素:  `p` , `div` , `h1~h6` , `form` , `hr` , `dl` , `ol` , `ul` , `table`;

- 常用行内元素: `span` , `a` , `br` , `code` , `i` , `em` , `img` , `input` ,`label` , `select` , `textarea`;

#### 2.split()和join()的区别
- `split()`: 一个数组调用这个方法,传入一个String参数,会返回由参数拼接而成的字符串;

- `join()`: 一个字符串调用这个方法,传入一个String参数,会返回由参数分割的数组;

#### 3.js的typeof()返回哪些数据类型
- `number` , `string` , `boolean` , `object` , `function` , `undefined`

#### 4.数组方法pop() push() unshift() shift()的区别
- `pop()`: 删除数组最末尾的值,返回值是被删除的值;

- `push()`: 在数组末尾添加传的参数,返回值是添加进去的值;

- `unshift()`: 在数组最前端插入传的参数,返回值是添加进去的值;

- `shift()`: 删除数组最前端的值,返回值是被删除的值;

#### 5.ajax请求的时候get和post方式的区别
- get: 参数会在url中显示,GET方式传送数据量小，处理效率高，安全性低，会被缓存;

- post: 浏览器会把所有表单字段作为参数发送给服务器,并不会显示在url中,可传送数据量大,安全性较好,不会被缓存;

#### 6.call和apply的区别
- `call()`: 作用是可以借用另一个对象的方法,从而改变方法的this指向.此方法有2个参数,第1个参数传入this指向的对象,第2个参数传入借用方法需要的参数,与 `apply` 的区别在于第2个参数, `call` 传递字符串类型的实参,当被借用方法所需的参数数量确定时用 `call`;

- `apply()`:`apply` 的第2个参数需要传递一个数组,并且会自动遍历数组里的参数一一传入所借用的方法,所借用方法的参数数量不定时用 `apply`;

#### 7.ajax请求时如何解析json数据
- `json.parse()`方法可以把json字符串解析为对象

#### 8.document.ready事件和document.load事件的区别
> 两者都是页面加载完成后触发的事件,区别在于 `document.ready` 表示文档结构加载完成,但是不包括图片等,而 `document.load` 则包括图片在内页面中所有的东西都加载完成后才触发

#### 9.xhtml和html有什么区别
> xhtml 的书写及代码都比 html 严格规范

#### 10.css引入的方式有哪些?link和import的区别是?
- 外联式,内联式,内嵌式,导入式;

- 区别:link除了加载css外还能定义RSS等其他事务;@import只能加载css,link支持使用js控制DOM改变样式;import不支持;

#### 11.前端页面有哪三层构成,分别是什么?作用是什么?
- 结构层:html,语义描述页面,负责页面的内容;

- 表示层:css,负责页面的样式;

- 行为层:js,负责页面的行为;

#### 12.css的基本语句构成是?
> 选择器{
  属性:属性值
  }

#### 13.你做的页面在哪些浏览器测试过?这些浏览器的内核分别是什么?
> 一般在chrome firefox IE上测试,他们的内核分别是Webkit,Gecko,Trident;

#### 14.谈谈JavaScript的本地对象,内置对象和宿主对象.
- 本地对象:就是那些官方定义好了的对象。
- 内置对象:是本地对象的一种，其只包含Global对象和Math对象。
- 宿主对象:则是那些官方未定义，你自己构建的对象加上DOM和BOM对象组成的。

#### 15.解释jsonp的原理,以及为什么不是真正的ajax?
> jsonp是通过 `script` 标签没有跨域限制的特性来实现跨域通信,其原理主要是创建一个 `script` 标签地址指向需跨域通信的地址,并提供一个回调函数来接收数据(函数名通过地址参数传递),这样浏览器会调用回调函数,并把解析后的json对象作为参数传入,本地就能通过回调函数获取到这个参数.

>因为数据传递过程不需要通过XHR对象来实现,所以不算真正的ajax.

#### 16.如何让div居中,如何居中一个浮动的元素？
- 方法一:
父盒子设置: position:relative;
子盒子设置: position:absolute; transform:translate(-50%,-50%); top:50%;  left:50%;

- 方法二:
父盒子设置: position:relative;
子盒子设置: position:absolute; top:0; left:0; right:0; bottom:0; margin:auto;

- 方法三:
父盒子设置: text-align:center; vertical-align:middle; display:table-cell;
子盒子设置: vertical-align:middle; display:inline-block;
- 方法一 和 方法二 都可以使浮动的盒子居中

#### 17.清除浮动的方式？各自的优缺点
- 方法一：父级定义height
 - 原理：父级div手动定义height，就解决了父级div无法自动获取到高度的问题
 - 优点：简单，代码少，容易掌握
 - 缺点：只适合高度固定的布局，要给出精确的高度，如果高度和父级div不一样时，会产生问题;
 - 建议：不推荐使用，只建议高度固定的布局时使用;


- 方法二：结尾处加空div标签clear:both
 - 原理：添加一个空div，利用css提高的clear:both清除浮动，让父级div能自动获取到高度
 - 优点：简单，代码少，浏览器支持好，不容易出现怪问题
 - 缺点：不少初学者不理解原理；如果页面浮动布局多，就要增加很多空div，让人感觉很不爽
 - 建议：不推荐使用，但此方法是以前主要使用的一种清除浮动方法;


- 方法三：父级div定义伪类:after和zoom
 - 原理：IE8以上和非IE浏览器才支持:after，原理和方法2有点类似，zoom(IE转有属性)可解决ie6,ie7浮动问题;
 - 优点：浏览器支持好，不容易出现怪问题（目前：大型网站都有使用，如：腾迅，网易，新浪等等）;
 - 缺点：代码多，不少初学者不理解原理，要两句代码结合使用，才能让主流浏览器都支持;
 - 建议：推荐使用，建议定义公共类，以减少CSS代码;


- 方法四：父级div定义overflow:hidden
 - 原理：必须定义width或zoom:1，同时不能定义height，使用overflow:hidden时，浏览器会自动检查浮动区域的高度
 - 优点：简单，代码少，浏览器支持好
 - 缺点：不能和position配合使用，因为超出的尺寸的会被隐藏
 - 建议：只推荐没有使用position或对overflow:hidden理解比较深的朋友使用;


- 方法五：父级div定义overflow:auto
 - 原理：必须定义width或zoom:1，同时不能定义height，使用overflow:auto时，浏览器会自动检查浮动区域的高度
 - 优点：简单，代码少，浏览器支持好
 - 缺点：内部宽高超过父级div时，会出现滚动条。
 - 建议：不推荐使用，如果你需要出现滚动条或者确保你的代码不会出现滚动条就使用吧。


- 方法六：父级div也一起浮动
 - 原理：所有代码一起浮动，就变成了一个整体
 - 优点：没有优点
 - 缺点：会产生新的浮动问题
 - 建议：不推荐使用，只作了解


- 方法七：父级div定义display:table
 - 原理：将div属性变成表格
 - 优点：没有优点
 - 缺点：会产生新的未知问题
 - 建议：不推荐使用，只作了解


- 方法八：结尾处加br标签clear:both
 - 原理：父级div定义zoom:1来解决IE浮动问题，结尾处加br标签clear:both
 - 建议：不推荐使用，只作了解

#### 18.css 和 @import 的区别
> 两者都是外部引用CSS的方式，但是存在一定的区别：

- link是XHTML标签，除了加载CSS外，还可以定义RSS等其他事务；@import属于CSS范畴，只能加载CSS。
- link引用CSS时，在页面载入时同时加载；@import需要页面网页完全载入以后加载。
- link是XHTML标签，无兼容问题；@import是在CSS2.1提出的，低版本的浏览器不支持。
- link支持使用Javascript控制DOM去改变样式；而@import不支持。


#### 19.图片标签上title与alt属性的区别是什么?
- `alt`:用于当图片加载失败时,图片显示区域显示的说明文本;

- `title`:表示当鼠标在图片上停留一段时间,显示的说明文本;

#### 20.请列举出你常用的减少页面加载时间的方法.
- 压缩Javascript、CSS代码;
- 引用的包都用CDN载入;
- 服务器开启gzip压缩;
- 优化图片尺寸;
- 小图标拼成精灵图使用;
- 按需加载,懒加载
- css样式放在页头
- js脚本放在页尾
- 减少DOM节点
- 模块化

#### 21.HTML5有哪些新标签
- `header`: 定义头部;

- `nav`: 定义通栏;

- `acticle`: 定义文章标题;

- `section`: 定义文章内容;

- `aside`:定义边栏;

- `footer`: 定义底部;

- `video`: 定义视频;

- `audio`: 定义音频;

- `canvas`: 定义画布;

- `source`:定义媒体文件;

#### 22.js变量类型有几种
- 简单类型：number、string、boolean、undefined、null
- 复杂类型：object

#### 23.写出你知道的http状态码
- 200 请求成功
- 304 自从上次请求后，请求的网页未修改过
- 503 服务器暂时不可用
- 400 请求错误
- 401 没有权限
- 403 forbidden 你的服务器或者主机禁止访问
- 404 找不到请求页面

#### 24.请问打印结果是什么？
```js
<script>
    for ( var i = 0; i < 10; i++ ) {
        window.setTimeout( function () {
            console.log( i ); //10个10
        }, 100 )
    }
    console.log( i ); //10
    var foo = 1,
        bar = 2,
        j, text;
    text = function ( j ) {
        j = 5;
        var bar = 5;
        foo = 5;
    }
    text( 10 );
    console.log( foo ); //5
    console.log( bar ); //2
    console.log( j ); //undefined
</script>
```

#### 25.js编程规范
- 命名规范：介绍变量、函数、常量、构造函数、类的成员等等的命名规范

- 注释规范：介绍单行注释、多行注释以及函数注释

- 框架开发：介绍全局变量冲突、单全局变量以及命名空间


#### 26.javascript中“use strict;”是什么意思？使用他的区别是什么
- 开启严格模式
- 不允许用with。
- 所有变量必须声明，赋值给未声明的变量报错，而不是隐匿创建全局变量。
- eval中的代码不能创建eval所在作用域下的变量、函数。而是为eval单独创建一个作用域，并在eval返回时丢弃。
- 函数中的特殊对象arguments是静态副本，而不像非严格模式那样，修改arguments或修改参数变量会相互影响。
- 删除configurable=false的属性时报错，而不是忽略。
- 对象字面量重复属性名报错。
- 禁止八进制字面量，如010（八进制的8）。
- 严格模式下eval、arguments变为关键字，不能用作变量名。
- 一般函数调用时（不是对象的方法调用，也不使用apply/call/bind等修改this）this指向null，而不是全局变量。
- 试图修改不可写属性（writable=false），在不可扩展的对象上添加属性时报TypeError，而不是忽略。
- arguments.caller,arguements.callee被禁用

#### 27.如何判断一个对象是否属于某个类？

#### 28.一个页面从输入url到页面加载完成这个过程都发生了什么？
- 输入地址
- 浏览器查找域名的 IP 地址
- 这一步包括 DNS 具体的查找过程，包括：浏览器缓存->系统缓存->路由器缓存...
- 浏览器向 web 服务器发送一个 HTTP 请求
- 服务器的永久重定向响应（从 http://example.com 到 http://www.example.com）
- 浏览器跟踪重定向地址
- 服务器处理请求
- 服务器返回一个 HTTP 响应
- 浏览器显示 HTML
- 浏览器发送请求获取嵌入在 HTML 中的资源（如图片、音频、视频、CSS、JS等等）
- 浏览器发送异步请求

#### 29.css3中background:rgba(255,0,0,0.5)中这些数字分别代表什么意思？
- 255代表red值，红色值
- 0代表green值，绿色值
- 第三个0代表蓝色值，blue
- 第四个数代表A，alpha，是透明度

#### 30.不同浏览器js方面的差异
- 1.firefox、chrome中没有window.event对象，只有event对象，而IE里是window.event对象;
- 2.Ajax请求 IE：new ActiveXObject(),firefox,chrome:new XMLHttpRequest();
- 3.firefox不支持innnerText，他支持textContent来实现innerText
- 4.获取可见区域、窗口的大小。有时，我们会需要找到浏览器的可视位置的大小，通常我们称之为"可见区域"。
- 在IE中这样写：document.documentElement.clientWidth;document.documentElement.clientHeight;
- 在Firefox中这样写：window.innerWidth;window.innerHeight;
- 5.获取鼠标指针的位置
- 在IE中这样写：event.clientX;event.clientY;在Firefox中这样写：event.pageX;event.pageY;

#### 31.css中display都有哪些常用的值?

- `display:none` 隐藏;

- `display:block` 块级元素;

- `display:inline` 行内元素;

- `display:inline-block` 行内块元素;

#### 32.css中都知道哪些选择器.

- id选择器 #id{};
- 类选择器 .class{};
- 标签选择器 标签{};
- 后代选择器 祖 (空格) 孙{};
- 子选择器 父>子{};
- 伪类选择器 a:hover{};
- 通配符选择器 \*{};
- 群选择器 标签,标签,标签{};
- 相邻兄弟选择器 兄弟1+兄弟2{};
- 属性选择器 [属性]{}
- 伪元素选择器 标签::after{}

#### 33.如何清除浮动元素造成的高度塌陷?
- 如果子元素全部浮动,给父元素设置高度(缺陷:一般开发中父盒子高度都是由内容撑开的,所以不常用);

- 为父元素添加`clear:both`(缺陷:会使2个父盒子之间的margin失效);

- 父元素设置`overflow:hidden`(缺陷:特殊情况下,如果子元素定位出了父元素,会因设置了`overflow:hidden`而被隐藏);

- 给父元素设置一个有`clear:both`属性并且宽高为0的透明伪元素来清除浮动(完美,现在的主流方法);



#### 35.简述css中伪元素和伪类有哪些?

- 伪类:
  - `:active`:将样式添加到被激活的元素;
  - `:focus`:将样式添加到被选中的元素;
  - `:hover`:当鼠标停留在上方时,向元素添加样式;
  - `:link`:给未被访问过的链接添加样式;
  - `:visited`:给已被访问过的链接添加样式;
  - `:first-child`:给元素的第一个子元素,添加样式;


- 伪元素:
  - `::first-letter`:给文本首字母添加样式;
  - `::first-line`:给文本首行添加样式;
  - `::before`:在元素之前插入样式;
  - `::after`:在元素之后插入样式;


#### 36.简述css的盒模型
> css的盒模型可以分为四个部分;
- element:此部分包含主内容,height,width;
- padding:此部分为element与border之间的填充;
- border:此部分为盒模型的边框;
- margin:此部分为两个盒模型之间的间距;

#### 37.css的hack有哪些?
- \9: ie678;
- \0: ie8;
- +: ie67;
- _: ie6;

#### 38.简述前端常用的布局方法.
- 固定布局:主内容给死一个固定的宽度,在大屏中显示页面左右会有大量的空白部分;

- 弹性布局:使用单位rem进行相对布局,可以灵活的根据屏幕的大小改变html字体大小来调整整体布局的大小;

- 流动布局:通过整体单位用%来进行相对布局, 可以根据父元素的实时尺寸来调整大小,配合max-width等属性来避免过大或过小导致阅读困难,某些情况下可能导致布局被破坏;

- 伸缩布局:使用css3 flex系列属性来布局,pc端兼容性较差还未普及;

- 响应式布局:通过`@media`媒体查询根据不同的屏幕大小切换布局的样式,对于内容较多的页面不适用;

- 自适应布局:通过媒体查询和流动布局搭配进行布局;
## 程序题

#### 1.排序算法(任选一种用js实现)

```js
var arr = [10, 5, 23, 0, 2];

    function sort(arr) {
        for (var i = 0; i < arr.length; i++) {
            for (var j = 0; j < arr.length - i; j++) {
                if (arr[j] > arr[j + 1]) {
                    var temp = arr[j];
                    arr[j] = arr[j + 1];
                    arr[j + 1] = temp;
                }
            }
        }
        return arr
    }

    console.log(sort(arr));
```

#### 2.写一个获取非行间样式的函数

```js
var div1 = document.getElementById("div1");
        alert(getstyle(div1, 'width'));

        function getstyle(obj, attr) {
            if (obj.currentStyle) {
                //兼容ie
                return obj.currentStyle[attr];
            } else {
                //现代浏览器
                return getComputedStyle(obj, false)[attr];
            }
        }
```
#### 3.有数组var arr=['a','b','c','1','0','c',1,'',1,0]请用js让unique(arr)返回['a','b','c','1','0',1,'',0].
```js
 var arr1 = ['a', 'b', 'c', '1', '0', 'c', 1, '', 1, 0];

    function unique(arr) {
        var newArr = [];
        for (var i = 0; i < arr.length; i++) {
            if (newArr.indexOf(arr[i]) == -1) {
                console.log(newArr.indexOf(arr[i] == -1))
                newArr.push(arr[i]);
            }
        }
        return newArr;
    }
    console.log(unique(arr1));
```
#### 4.css布局，左边宽度自适应，右边宽度设置200px
```html
    <style>
        .bigbox {
            height: 200px;
            margin: 0px 400px;
            border: 1px solid black;
        }

        .left {
            height: 100%;
            background-color: pink;
        }

        .right {
            float: right;
            width: 200px;
            height: 100%;
            background-color: red;
            }
    </style>

    <body>
      <div class="bigbox">
        <div class="right"></div>
        <div class="left"></div>
      </div>
    </body>
```

#### 5.css布局，两列等高，高度自适应(品字布局)
```html
<style>
    html,
    body {
        margin: 0;
        padding: 0;
        height: 100%;
    }

    div:first-child {
        width: 100%;
        height: 200px;
        background: red;
    }

    div:nth-child(2) {
        position: fixed;
        width: 50%;
        height: calc(100% - 200px);
        background: green;
        bottom: 0;
        left: 0;
    }

    div:nth-child(3) {
        position: fixed;
        width: 50%;
        height: calc(100% - 200px);
        background: yellow;
        bottom: 0;
        right: 0;
    }
</style>
```

#### 6.如何判断js对象是否存在？
```js
//暂写8种方式
    <script>
        var myObj;
        if ( !myObj ) {
            console.log( '不存在' );
        }

        if ( typeof myObj != 'object' ) {
            console.log( '不存在' );
        }

        if ( typeof myObj == 'undefined' )        {
            console.log( '不存在' );
        }

        if ( !window.myObj ) {
            console.log( '不存在' );
        }

        if ( !this.myObj ) {
            console.log( '不存在' );
        }

        if ( myObj == null ) {
            console.log( '不存在' );
        }

        if ( myObj == undefined ) {
            console.log( '不存在' );
        }

        if ( myObj === undefined ) {
            console.log( '不存在' );
        }
    </script>
```
#### 7.当文档宽度小于300像素则修改背景颜色,如何实现?
```html
<style>
    body {
        background-color: blue;
    }

    @media screen and (max-width:300px) {
        body {
            background-color: red;
        }
    }
</style>
```
#### 8.如何将字符串string2附加到string1?
```js
        var str1 = '你好';
        var str2 = '世界';
        str1 = str1.concat(str2);
        console.log(str1);
```
#### 9.设置一个已知ID的DIV的html内容为xxxx,字体颜色设置为黑色
```js
        var box = document.getElementById('box');
        box.innerHTML = 'xxxx';
        box.style.color = '#000';
```
#### 10.如何设置,获取和删除cookie
```js
        //设置cookie
        document.cookie = 'hello world';
        //获取cookie
        console.log(document.cookie);
        //删除cookie
        document.cookie = '';
```

#### 11.已知ID的input输入框,怎么获取这个输入框的输入值?
```js
        var user = document.getElementById('user');
        user.addEventListener('keyup', function() {
        //当键盘弹起时就能获取这个输入框中的值
            console.log(user.value);
        })

```
#### 12.如何判断所使用的浏览器是否直接支持JSON?


#### 13.用正则完全删除与某个字符串相同相邻的字符‘郑复兵兵++5656’;

#### 14.手写insertafter方法插入节点
```js
        function insertAfter( newChild, refChild ) {
            var parent = refChild.parentNode;
            if ( refChild === parent.lastChild ) {
                parent.appendChild( newChild );
            } else {
                parent.insertBefore( newChild, refChild.nextSibling );
            }
        }
```

#### 15.用js生成一个表格
```js
        var table = '<table>' +
            '<tr>' +
            '<td>年龄</td>' +
            '<td>性别</td>' +
            '<td>名字</td>' +
            '</tr>' +
            '<tr>' +
            '<td>16</td>' +
            '<td>男</td>' +
            '<td>ls</td>' +
            '</tr>' +
            '<tr>' +
            '<td>28</td>' +
            '<td>男</td>' +
            '<td>zs</td>' +
            '</tr>' +
            '</table>';

        document.querySelector( 'body' ).innerHTML = table;
```

#### 16.请写一个函数,接受摄氏度作为参数,返回相应的华氏度.
> 华氏度(℉)=32+摄氏度(℃)×<1 class="8"></1>

```js
 //公式:华氏度(℉)=32+摄氏度(℃)×1.8
        function temp(degree) {
            var f = 0;
            var c = degree;
            f = 32 + (c * 1.8);
            return f;
        }
        console.log(temp(5));
```

#### 17.下面这个ul,如何点击每一列的时候弹出其index.
```js
        var lis = document.querySelectorAll('li');
                for (var i = 0; i < lis.length; i++) {
            lis[i].setAttribute('index', i);
            lis[i].addEventListener('click', function() {;
                console.log(this.getAttribute('index'));
            });
        }
```

#### 18.[ "1", "2", "3" ].map( parseInt )返回结果是什么？
```js
    <script>
        var r = [ "1", "2", "3" ].map( parseInt );
        console.log( r );
        // map() 方法返回一个由原数组中的每个元素调用一个指定方法后的返回值组成的新数组。
        // 那么[ "1", "2", "3" ].map( parseInt )返回值是什么呢？
        // 你一定会觉得返回值是[1,2,3];
        // 实际返回结果是[1,NaN,NaN];
        // 为什么呢？
        // 其实parseInt是有3个参数的,第二个参数是进制,第三个参数会被parseInt忽视;
        // parseInt会把传过来的索引值当作进制数使用
        // parseInt("1",0),parseInt("2",1),parseInt("3",2)
    </script>
```
#### 19.js中如何创建新数组并初始化.
```js
        var arr = [1, 2, 3];
        var arrNew = new Array(4, 5, 6);
        console.log(arr);
        console.log(arrNew);
```
#### 20.合并两个数组，a = [0,1,2];b = [a,b,c],并且删除新数组的第二个元素
```js
    <script>
        var a = [ 0, 1, 2 ];
        var b = [ 'a', 'b', 'c' ];
        var newArr = a.concat( b );
        newArr.splice( 1, 1 );
        console.log( newArr )
    </script>
```

#### 21.获取DOM元素的位置
> offsetParent属性返回一个对象的引用，这个对象是距离调用offsetParent的元素最近的（在包含层次中最靠近的），并且是已进行过CSS定位的容器元素。

```js
    function getElemPos( obj ) {
        var pos = {
            "top": 0,
            "left": 0
        };
        if ( obj.offsetParent ) {
            while ( obj.offsetParent ) {
                pos.top += obj.offsetTop;
                pos.left += obj.offsetLeft;
                obj = obj.offsetParent;
            }
        } else if ( obj.x ) {
            pos.left += obj.x;
        } else if ( obj.x ) {
            pos.top += obj.y;
        }
        return {
            x: pos.left,
            y: pos.top
        };
    }
```

#### 22.css中常用居中技术(水平和垂直)有哪些?
```js
//当父元素为块级元素并指定宽高,子元素为行内元素时:

//方法一:
.father{
            text-align: center;
            line-height: 500px;//和高度一样
        }

//当父元素为块级元素并指定宽高,子元素为块级元素时:

//方法一:
.father{
            display: table-cell;
            vertical-align: middle;
        }
.son{
			margin: 0 auto;
        }

//方法二:
.father{
            position: relative;

        }
		
.son{
            position: absolute;
            left: 50%;
            top: 50%;
            margin: -50px;//总宽度的一半
        }
```

