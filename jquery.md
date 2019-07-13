[TOC]



#### 在 DOM 加载完成后运行

```js
$(document).ready(function(){
   // 开始写 jQuery 代码...
});
```

**简写**

```js
$(function(){
   // 开始写 jQuery 代码...
});
```



## 选择器

#### 元素选择器

在页面中选取所有 <p> 元素

``` $("p") ```

```js
$(document).ready(function(){
  $("button").click(function(){
    $("p").hide();
  });
});
```



#### #id 选择器

通过 id 选取元素语法如下

``` $("#test") ```

```js
$(document).ready(function(){
  $("button").click(function(){
    $("#test").hide();
  });
});
```

## 

#### .class 选择器

``` $(".test") ```

```js
$(document).ready(function(){
  $("button").click(function(){
    $(".test").hide();
  });
});
```



#### 其它选择器

| 语法                     | 描述                                                    |
| ------------------------ | ------------------------------------------------------- |
| $("*")                   | 选取所有元素                                            |
| $(this)                  | 选取当前 HTML 元素                                      |
| $("p.intro")             | 选取 class 为 intro 的 <p> 元素                         |
| $("p:first")             | 选取第一个 <p> 元素                                     |
| $("ul li:first")         | 选取第一个 <ul> 元素的第一个 <li> 元素                  |
| $("ul li:first-child")   | 选取每个 <ul> 元素的第一个 <li> 元素                    |
| $("[href]")              | 选取带有 href 属性的元素                                |
| $("a[target='_blank']")  | 选取所有 target 属性值等于 "_blank" 的 <a> 元素         |
| $("a[target!='_blank']") | 选取所有 target 属性值不等于 "_blank" 的 <a> 元素       |
| $(":button")             | 选取所有 type="button" 的 <input> 元素 和 <button> 元素 |
| $("tr:even")             | 选取偶数位置的 <tr> 元素                                |
| $("tr:odd")              | 选取奇数位置的 <tr> 元素                                |





## 事件

#### click()

click() 方法是当按钮点击事件被触发时会调用一个函数。

```js
$("p").click(function(){
  $(this).hide();
});
```



#### dblclick()

当双击元素时，会发生 dblclick 事件。

```js
$("p").dblclick(function(){
  $(this).hide();
});
```



#### mouseenter()

当鼠标指针穿过元素时，会发生 mouseenter 事件。

```js
$("#p1").mouseenter(function(){
    alert('您的鼠标移到了 id="p1" 的元素上!');
});
```



#### mouseleave()

当鼠标指针离开元素时，会发生 mouseleave 事件。

```js
$("#p1").mouseleave(function(){
    alert("再见，您的鼠标离开了该段落。");
});
```



#### mousedown()

当鼠标指针移动到元素上方，并按下鼠标按键时，会发生 mousedown 事件。

```js
$("#p1").mousedown(function(){
    alert("鼠标在该段落上按下！");
});
```



#### mouseup()

当在元素上松开鼠标按钮时，会发生 mouseup 事件。

```js
$("#p1").mouseup(function(){
    alert("鼠标在段落上松开。");
});
```



#### hover()

hover()方法用于模拟光标悬停事件。

当鼠标移动到元素上时，会触发指定的第一个函数(mouseenter);当鼠标移出这个元素时，会触发指定的第二个函数(mouseleave)。

```js
$("#p1").hover(
    function(){
        alert("你进入了 p1!");
    },
    function(){
        alert("拜拜! 现在你离开了 p1!");
    }
);
```



#### focus()

当元素获得焦点时，发生 focus 事件。

当通过鼠标点击选中元素或通过 tab 键定位到元素时，该元素就会获得焦点。

focus() 方法触发 focus 事件，或规定当发生 focus 事件时运行的函数：

```js
$("input").focus(function(){
  $(this).css("background-color","#cccccc");
});
```



#### blur()

当元素失去焦点时，发生 blur 事件。

```js
$("input").blur(function(){
  $(this).css("background-color","#ffffff");
});
```







## 获取和设置内容

- text() - 设置或返回所选元素的文本内容
- html() - 设置或返回所选元素的内容（包括 HTML 标记）
- val() - 设置或返回表单字段的值

```js
$("#button").click(function(){
    // 获取p标签内容, 只会获取内容, 会过滤掉html标签, 多级html效果会明显
    console.log( $("p").text() );
    // 获取p标签内容, 子标签及内容会一起获取到
    console.log( $("p").html() );
    
    // 设置元素内容
    $("h3").text("hello h3");
    $("h4").html("hello h4");
    
    // 获取表单字段的值
    $("#user").val();
    
    // 设置表单的值
    console.log( $("#age").val(25) );
})
```







#### 获取属性 - attr()

获得链接中 href 属性的值

```js
$("button").click(function(){
  alert($("#runoob").attr("href"));
});
```







## 添加元素

#### 添加新的 HTML 内容

- append() - 在被选元素的结尾插入内容
- prepend() - 在被选元素的开头插入内容
- after() - 在被选元素之后插入内容
- before() - 在被选元素之前插入内容



#### append() 方法

jQuery append() 方法在被选元素的结尾插入内容（仍然该元素的内部）。

```js
$("p").append("追加文本");
```



#### prepend() 方法

jQuery prepend() 方法在被选元素的开头插入内容。

```js
$("p").prepend("在开头追加文本");
```



#### 通过 append() 和 prepend() 方法添加若干新元素

在上面的例子中，我们只在被选元素的开头/结尾插入文本/HTML。

不过，append() 和 prepend() 方法能够通过参数接收无限数量的新元素。可以通过 jQuery 来生成文本/HTML（就像上面的例子那样），或者通过 JavaScript 代码和 DOM 元素。

在下面的例子中，我们创建若干个新元素。这些元素可以通过 text/HTML、jQuery 或者 JavaScript/DOM 来创建。然后我们通过 append() 方法把这些新元素追加到文本中（对 prepend() 同样有效）：

```js
function appendText()
{
    var txt1="<p>文本。</p>";              // 使用 HTML 标签创建文本
    var txt2=$("<p></p>").text("文本。");  // 使用 jQuery 创建文本
    var txt3=document.createElement("p");
    txt3.innerHTML="文本。";               // 使用 DOM 创建文本 text with DOM
    $("body").append(txt1,txt2,txt3);        // 追加新元素
}
```



#### after() 和 before() 方法

after() 方法在被选元素之后插入内容。

before() 方法在被选元素之前插入内容。

```js
$("img").after("在后面添加文本");
 
$("img").before("在前面添加文本");
```





#### 通过 after() 和 before() 方法添加若干新元素

after() 和 before() 方法能够通过参数接收无限数量的新元素。可以通过 text/HTML、jQuery 或者 JavaScript/DOM 来创建新元素。

在下面的例子中，我们创建若干新元素。这些元素可以通过 text/HTML、jQuery 或者 JavaScript/DOM 来创建。然后我们通过 after() 方法把这些新元素插到文本中（对 before() 同样有效）：

```js
function afterText()
{
    var txt1="<b>I </b>";                    // 使用 HTML 创建元素
    var txt2=$("<i></i>").text("love ");     // 使用 jQuery 创建元素
    var txt3=document.createElement("big");  // 使用 DOM 创建元素
    txt3.innerHTML="jQuery!";
    $("img").after(txt1,txt2,txt3);          // 在图片后添加文本
}
```





## 删除元素

- remove() - 删除被选元素（及其子元素）
- empty() - 从被选元素中删除子元素



#### remove() 方法

remove() 方法删除被选元素及其子元素。

```js
$("#div1").remove();
```



#### empty() 方法

empty() 方法删除被选元素的子元素。

```js
$("#div1").empty();
```



#### 过滤被删除的元素

remove() 方法也可接受一个参数，允许您对被删元素进行过滤。

该参数可以是任何 jQuery 选择器的语法。

下面的例子删除 class="italic" 的所有 <p> 元素：

```js
$("p").remove(".italic");
```





## 获取并设置 CSS 类

- addClass() - 向被选元素添加一个或多个类
- removeClass() - 从被选元素删除一个或多个类
- toggleClass() - 对被选元素进行添加/删除类的切换操作
- css() - 设置或返回样式属性



示例样式表

```css
.important
{
        font-weight:bold;
        font-size:xx-large;
}
 
.blue
{
        color:blue;
}
```

#### addClass() 方法

向不同的元素添加 class 属性。当然，在添加类时，您也可以选取多个元素：

```js
$("button").click(function(){
  $("h1,h2,p").addClass("blue");
  $("div").addClass("important");
});
```

在 addClass() 方法中规定多个类：

```js
$("button").click(function(){
  $("body div:first").addClass("important blue");
});
```



#### removeClass() 方法

在不同的元素中删除指定的 class 属性：

```js
$("button").click(function(){
  $("h1,h2,p").removeClass("blue");
});
```



#### toggleClass() 方法

使用 toggleClass() 方法。该方法对被选元素进行添加/删除类的切换操作：

```js
$("button").click(function(){
  $("h1,h2,p").toggleClass("blue");
});
```





## 操作CSS

#### css() 方法

css() 方法设置或返回被选元素的一个或多个样式属性。

#### 返回 CSS 属性

``` css("*propertyname*");``` 

下面的例子将返回首个匹配元素的 background-color 值：

```js
$("p").css("background-color");
```



#### 设置 CSS 属性

``` css("*propertyname*","*value*"); ```

下面的例子将为所有匹配元素设置 background-color 值：

```js
$("p").css("background-color","yellow");
```



#### 设置多个 CSS 属性

``` css({"*propertyname*":"*value*","*propertyname*":"*value*",...}); ```

下面的例子将为所有匹配元素设置 background-color 和 font-size：

```js
$("p").css({"background-color":"yellow","font-size":"200%"});
```





## AJAX

#### 请求示例

```html
<script type=text/javascript>
    $(document).ready(function () {
        $("#submit").click(function () {
            $.ajax({
                url: '/test',
                type: 'GET',
                async: true,
                data: {
                    username: 'king',
                    password: '111111'
                },
                timeout: 5000,
                dataType: 'json',
                beforeSend: function (xhr) {
                    console.log(xhr);
                    console.log('发送前');
                },
                success: function (data, textStatus, jqXHR) {
                    console.log(data);
                    console.log(textStatus);
                    console.log(jqXHR);
                },
                error: function (xhr, textStatus) {
                    console.log('错误');
                    console.log(xhr);
                    console.log(textStatus);
                },
                complete: function () {
                    console.log('结束');
                }
            })
        });
    });
</script>
```

