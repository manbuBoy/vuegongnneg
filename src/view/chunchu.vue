<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
        <title>session</title>
        <script src="https://unpkg.com/vue/dist/vue.js"></script>
        <style type="text/css">
            #session {
                width: 600px;
                margin: 0 auto;
                text-align: center;
            }
        </style>
    </head>
    <body>
        <div id="session">
            <input type="text" v-on:keyup.enter="addNew()" v-model="inputValue" placeholder="请输入要保存的数据"/>
            <ul>
                <li v-for="item in items">{{ item.name }}</li>
            </ul>
        </div>
        
        <script>
            var storeKey = "studentName";
            var storage = {
                fetch:function(){
                    return JSON.parse(sessionStorage.getItem(storeKey) || "[]")
                },
                save:function(items){
                    console.log("00001");
                    sessionStorage.setItem(storeKey,JSON.stringify(items));
                }
            }
            var vm = new Vue({
                el:"#session",
                data:{
                    items:storage.fetch(),
                    inputValue:""
                },
                methods:{
                    //向数组添加内容
                    addNew:function(){
                        this.items.push({
                            name:this.inputValue
                        }),
                        this.inputValue = null
                    }
                },
                watch:{
                    //监听items的变化
                    items:{
                        handler:function(items){
                            storage.save(items);
                        },
                        deep:true
                    }
                }
            })
        </script>
    </body>
</html>