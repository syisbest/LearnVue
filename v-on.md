# v-on

使用v-on绑定点击事件，翻转函数使用`.split('').reverse().join('')`

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>v-on</title>
</head>
<body>
    <div id="app">
        <h3>{{message}}</h3>
        <button v-on:click="reverseMessage">翻转</button>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
    <script>
        var app=new Vue({
            el:'#app',
            data:{
                message:'hello Vue 你好',
            },
            methods:{
                reverseMessage:function(){
                    this.message=this.message.split('').reverse().join('');
                }
            }
        })
    </script>
</body>
</html>
```

