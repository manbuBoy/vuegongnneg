<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <Emlementtab />
    <Emlementtab1 />
    <IviewUpEmage />
    <Fenxiang />
    <DaTu />
    <StoreMassege />
    <router-view/>
   
  </div>
</template>

<script>
// eslint-disable-next-line no-unused-vars
import Emlementtab from './view/emlement-tab'
import Emlementtab1 from './view/emlement-tab1'
import IviewUpEmage from './view/iview-upEmage'
import Fenxiang from './view/fenxiang'
import DaTu from './view/daTu'
import StoreMassege from './view/storeMassege'
// import Demo1 from './view/tsdemo/demo1'
export default {
  name: 'App',
  components: {
    Emlementtab,
    Emlementtab1,
    IviewUpEmage,
    Fenxiang,
    DaTu,
    StoreMassege,
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
