# v-if

使用`v-if`来控制一个元素的显示和隐藏，添加一个按钮来控制，使用的是`v-on:click` 点击事件来改变seen的值

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>v-if</title>
</head>
<body>
    <div id="app">
        <p v-if="seen">看我</p>
        <button v-on:click="see">显示/隐藏</button>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
    <script>
        var app=new Vue({
        el:'#app',
        data:{
            seen:true
        },
        methods:{
            see:function(){
                this.seen=!this.seen;
            }
        }
    })
    </script>
</body>
</html>
```

