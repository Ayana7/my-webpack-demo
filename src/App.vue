<template>
  <div id="app">
    <router-view class="view"></router-view>
  </div>
</template>

<script>
import Hello from './components/Hello'

export default {
  name: 'app'
}
</script>

<style scoped lang="scss">
  @import "~normalize.css/normalize.css";
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

</style>
