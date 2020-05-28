<template>
 <div @click="changeStore">
    name:
    <h1>{{ $store.state.name }}</h1>
  </div>
</template>>
<script>
export default {
  data(){
    return{
    }
  },
  methods:{
    changeStore(){
        this.$store.dispatch('aEdit',{age:15})
      }
    }
  
}
</script>>
<style>

</style>