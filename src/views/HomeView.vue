<template>
  <div class="home-view">
    <he-nav></he-nav>
    <List></List>
  </div>
</template>

<script>
  import HeNav from '../components/HeNav.vue'
  import List from '../components/List.vue'
  export default {
    name: 'home-view',
    components: { HeNav, List}
  }
</script>

<style scoped=""></style>
