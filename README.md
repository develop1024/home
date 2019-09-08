

## Superman

![图片alt](./imgs/Spider-Man.png ''Superman'')

## Navigation


* [TodoDemo](https://develop1024.github.io/home/todolist.html){:target="_blank"}  
* [Linux添加桌面图标](https://develop1024.github.io/home/linuxAddDesktopIcon.html){:target="_blank"}  
* [MAC系统字体](#MAC系统字体)  
* [代码高亮显示](#代码高亮显示) 
* [golang交叉编译](https://develop1024.github.io/home/GoPlatformBuild.html){:target="_blank"}  




## MAC系统字体

[华文细黑](https://develop1024.github.io/home/fonts/huawenxihei.ttf) 适合中文字体使用  
[MONACO](https://develop1024.github.io/home/fonts/MONACO.TTF) 适合作为编程字体使用



## 代码高亮显示

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


## jQuery请求github api 
* [Jquery请求github api](https://develop1024.github.io/home/githubforuserinfo.html){:target="_blank"}  


## Dplqyer 播放器
* [Dplqyer 播放器示例](https://develop1024.github.io/home/dplayerDemo.html){:target="_blank"}  


## VS Code主题配色
``` Dracula Soft ```

## 生成ssh密钥
```
ssh-keygen -t rsa -C '656562721@qq.com'
```

## git基本使用
```
git 全局设置
git config --global user.name "develop1024"
git config --global user.email "656562721@qq.com"

提交一个本地仓库到云仓库
git init
touch README.md
git add README.md (提交全部 .)
git commit -m "first commit"
git remote add origin git@gitee.com:develop1024/blog.git
git push -u origin master
```


## 取golang模板

`
{{ index $val 1 }}
`


## 选颜色
https://flatuicolors.com/


## linux制作win启动盘工具woeusb
``` 格式化为NTFS ```

```
sudo add-apt-repository ppa:nilarimogard/webupd8
sudo apt update
sudo apt install woeusb
```

## 字符串转json

* [字符串转json](https://develop1024.github.io/home/tojson.html){:target="_blank"}  

