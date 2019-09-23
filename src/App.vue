<template>
  <div id="app">
    <TabBar/>
    <router-view/>
  </div>
</template>
<script>
import TabBar from './components/tabbar'
export default {
  name:"app",
  components:{
    TabBar
  }
}
</script>
<style lang="scss">
@import "./assets/css/reset.css";
</style>
