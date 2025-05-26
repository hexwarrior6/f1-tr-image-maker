<template>
  <div id="app">
    <DriverRadio />
  </div>
</template>

<script>
import DriverRadio from './components/DriverRadio.vue'
// 确保这些组件已经创建并在 DriverRadio 中使用了正确的名称
export default {
  name: 'App',
  components: {
    DriverRadio
  }
}
</script>

<style>
/* 可选：全局样式 */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>