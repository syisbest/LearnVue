# v-for

使用v-for来遍历数据

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>v-for</title>
</head>
<body>
    <div id="app">
        <ol>
            <li v-for="city in citys">
                {{city}}
            </li>
        </ol>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
    <script>
        var app=new Vue({
            el:'#app',
            data:{
                citys:['仙桃','武汉','宝鸡','西安'],
            },
        })
    </script>
</body>
</html>
```

