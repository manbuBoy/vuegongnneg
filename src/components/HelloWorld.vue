<template>
  <div class="hello">
    <Qr :value="msg" :isShow="isShow" :backFunction='funValue' />
    <button @click="changeValue">按下</button>
    <button @click="changeShow">让二维码显示</button>
    <button @click="lookF">看看子组件做了什么</button>
  </div>
  
</template>

<script>
import Qr from './qr.vue'
export default {
  name: 'HelloWorld',
  components:{
    Qr
  },
  data () {
    return {
      isvalue:false,
      isShow:false,
      msg: 'Welcome to Your Vue.js App',
      fff:Function,
      z:Function

    }
  },
  methods:{
    changeValue(){
      if(this.isvalue){
        this.msg = '我都们都变了'
        this.isvalue=!this.isvalue
      }else{
        this.msg = '其实你错了'
        this.isvalue=!this.isvalue
      }
    },
    changeShow(){
      this.isShow = !this.isShow
    },
    funValue(object){
      console.log('我被子组件调用了')
      console.log('子组件传值过来了',object)
      // this.fff = object.newFuntion
      this.z = object.zi
    },
    lookF(){
    //  this.fff()
    //  console.log(value)
     console.log('还真成了')
     this.z()
    }

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
