<template>
  <div id="app">
    <!-- 导入组件 -->
    <!-- <img src="./assets/logo.png">
    <router-view/> -->
    <eventDemo/>
  </div>
</template>

<script>
// import demo from './components/demo.vue'
// import computedDemo from './components/computedDemo.vue'
// import watchDemo from './components/watchDemo.vue'
// import classDemo from './components/classDemo'
// import ConditionDemo from './components/ConditionDemo'
// import ListDemo from './components/ListDemo'
import eventDemo from './components/eventDemo'
export default {
  name: 'App',
  components: {
    eventDemo
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
