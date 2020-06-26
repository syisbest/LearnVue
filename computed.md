# computed

翻转内容代码，和之前不同的是函数写在computed里面，表示计算属性，**计算属性是基于它们的响应式依赖进行缓存的**，还可以在computed里面写set函数，来给元素赋值。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>computed</title>
</head>
<body>
    <div id="app">
        <p>{{message}}</p>
        <p>{{reverseMessage}}</p>
        <p>{{nowDate}}</p>
        <p>{{now()}}</p>
        <p>{{fullName}}</p>
    </div>
    <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
    <script>
        var vm=new Vue({
            el:'#app',
            data:{
                message:'hello Vue 你好',
                firstName:'shen',
                lastName:'yan',
            },
            methods:{
                now:function(){
                    return Date.now();
                }
            },
            computed:{
                reverseMessage:function(){
                    return this.message.split('').reverse().join('');
                },
                nowDate:function(){
                    return Date.now();
                },
                fullName:{
                    get:function(){
                        return this.firstName+' '+this.lastName;
                    },
                    set:function(newName){
                        var name = newName.split(' ');
                        this.firstName=name[0];
                        this.lastName=name[name.length-1];
                    }
                }
            }
        })
    </script>
</body>
</html>
```

