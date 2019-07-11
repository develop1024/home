## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/develop1024/home/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/develop1024/home/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.



#### Vue.js todo
``` todo.html ```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>todu</title>
</head>
<body>
    <div id="app">
        <h1>任务列表</h1>
        <input type="text" v-model="task" placeholder="添加新任务.."> <button @click="addtolist">添加</button>

        <template v-for="task in undone">
            <template v-if="!task.done">
                <p>{{task.name}} <input type="checkbox" v-model="task.done">我做完了</p>
            </template>
            <template v-else>
                <p style="text-decoration: line-through">{{task.name}} <input type="checkbox" v-model="task.done">已做完</p>
            </template>
        </template>
        <hr>


    </div>
    <script src="node_modules/vue/dist/vue.js"></script>
    <script>
        new Vue({
            el: '#app',
            data: {
                task: '',
                undone: [],
            },
            methods: {
                addtolist(){
                    if(this.task!=''){
                        this.undone.push({name:this.task, done: false});
                        this.task = '';
                    }
                }
            }
        })
    </script>
</body>
</html>
```