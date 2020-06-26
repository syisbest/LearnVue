# v-model

使用v-model来实现输入

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>v-model</title>
</head>
<body>
    <div id="app">
        <h3>{{message}}</h3>
        <input type="text" v-model="message">
    </div>
    <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
    <script>
        var app=new Vue({
            el:'#app',
            data:{
                message:'hello Vue 你好',
            },
        })
    </script>
</body>
</html>
```

