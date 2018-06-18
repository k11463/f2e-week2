<template>
  <div id="app">
    <Navbar></Navbar>
    <router-view></router-view>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar.vue'
import Home from '@/components/Home.vue' //需要引入components才能使用elementUI
export default {
  el: '#app',
  components: {
    Navbar,
    Home,
  }
}
</script>

<style lang="scss">
@import '~pretty-checkbox/src/pretty-checkbox.scss';
*{
  padding: 0;
  margin: 0;
}
</style>
