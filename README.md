

## Welcome to My Pages

![图片alt](./imgs/Spider-Man.gif ''Superman'')

# Superman

[常用配置及例子](##常用配置及例子)
[Linux添加桌面图标](##Linux添加桌面图标)
[MAC系统字体](##MAC系统字体)
[HTML中代码高亮显示 highlightjs](##HTML中代码高亮显示 highlightjs)
[golang 交叉编译](##golang 交叉编译)



## 常用配置及例子

* Vue Todo 小例子

[Todo Demo](https://develop1024.github.io/home/todolist.html){:target="_blank"}



## Linux添加桌面图标

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


## MAC系统字体

[华文细黑](https://develop1024.github.io/home/fonts/huawenxihei.ttf) 适合中文字体使用  
[MONACO](https://develop1024.github.io/home/fonts/MONACO.TTF) 适合作为编程字体使用



## HTML中代码高亮显示 highlightjs

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


## golang 交叉编译

1.切换到项目工程的源码目录   

2.选择相应平台组合, 编译程序

```
CGO_ENABLED=0 GOOS=windows GOARCH=amd64 go build
```

CGO_ENABLED关闭CGO，GOOS设置目标操作系统，GOARCH设置目标架构  

可组合有如下

```
$GOOS        $GOARCH
android     arm
darwin      386
darwin      amd64
darwin      arm
darwin      arm64
dragonfly   amd64
freebsd     386
freebsd     amd64
freebsd     arm
linux       386
linux       amd64
linux       arm
linux       arm64
linux       ppc64
linux       ppc64le
linux       mips
linux       mipsle
linux       mips64
linux       mips64le
netbsd      386
netbsd      amd64
netbsd      arm
openbsd     386
openbsd     amd64
openbsd     arm
plan9       386
plan9       amd64
solaris     amd64
windows     386
windows     amd64
```



