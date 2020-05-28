<template>
  <div class="hello">
    <div v-show="isShow" id="qrcode">
      {{value}}
    </div>
    <button @click="backFunction(obj)">调用子组件的方法</button>
  </div>
</template>

<script>
import QRCode from 'qrcodejs2'
export default {
  name: 'HelloWorld',
  props:{
    value:{
      type:String,
      required:true
    },
    isShow:{
      type:Boolean,
      required:true
    },
    backFunction:{
      type:Function,
      required:true
    }
  },
  data () {
    return {
      msg: '二维码',
      obj:{},
    }
  },
  mounted(){
    console.log(
      '父组件向子组件传值',this.value,
      '父组件向子组件传布尔值',this.isShow
      )
    this.qrcode()
    this.obj={
      value:this.value,
      isShow:this.isShow,
      // newFuntion:function(){
      //   const newValue= '父组件调用了';
      //   console.log('我做了一些事情，把父组件的方法还给你了')
      //   this.backFunction(newValue)
      // },
      zi:this.ziF
    }
  },
  methods:{
    qrcode() { 
      let qrcode = new QRCode('qrcode', {
        width: 132,  
        height: 132,
        text: 'https://www.baidu.com', // 二维码地址
        colorDark : "#000",
        colorLight : "#fff",
      })
    },
    ziF(){
      console.log('我是子组件的方法') 
    }
  }
}
</script>
<style>
#qrcode {
  display: flex;
  align-items: center;
  justify-content: center;
}


</style>