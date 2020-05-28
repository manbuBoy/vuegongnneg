<template>
  <viewer :images="photo"> 
        //photo 一定要一个数组，否则报错
            <img
              v-for="(src,index) in photo"
              :src="src"
              :key="index"
              :onerror="errorImg"
            >
  </viewer>
  
</template>>
<script>
export default {
  data(){
    return{
      photo:[
       'http://img2.imgtn.bdimg.com/it/u=2462146637,4274174245&fm=26&gp=0.jpg',
        'http://img2.imgtn.bdimg.com/it/u=2462146637,4274174245&fm=26&gp=0.jpg'
      ]
    }
  }
  
}
</script>>
<style>

</style>