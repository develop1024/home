## Welcome to My Pages


#### 常用配置及例子

* Vue Todo 小例子

[Todo Demo](https://develop1024.github.io/home/todolist.html){:target="_blank"}



#### Linux添加桌面图标

``` vim /usr/share/applications/youapp.desktop ```

```ini
[Desktop Entry]
Name=goland
Exec=/usr/local/goland/bin/goland.sh
Comment=goland
Icon=/usr/local/goland/bin/goland.png
Type=Application
Terminal=false
Encoding=UTF-8
Categories=Developer;
```


#### MAC系统字体

[华文细黑](https://develop1024.github.io/home/fonts/huawenxihei.ttf) 适合中文字体使用  
[MONACO](https://develop1024.github.io/home/fonts/MONACO.TTF) 适合作为编程字体使用



#### HTML中代码高亮显示 highlightjs

[highlightjs Demo](https://develop1024.github.io/home/highlight_test.html){:target="_blank"}  
[highlightjs](https://highlightjs.org/){:target="_blank"}


* 使用方式

1.引入highlight的js文件和css样式文件
```html
<link rel="stylesheet" href="highlight/styles/magula.css">
<script src="highlight/highlight.pack.js"></script>
```

2.设置你的语言类型
```html
<pre><code class="html">这里就是要显示高亮的代码</code></pre>
```

3.让代码自动高亮
```html
<script>hljs.initHighlightingOnLoad();</script>
```