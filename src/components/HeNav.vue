<template>
  <div class="he-nav has-header">
    <ul class="quick-nav">
      <li>
        <router-link :to="{name: 'MovieView'}">影院热映</router-link>
      </li>
      <li>
        <router-link :to="{ name: 'BookView'}">图书</router-link>
      </li>
      <li>
        <router-link :to="{ name: 'StatusView'}">欧美新碟榜</router-link>
      </li>
      <li>
        <router-link :to="{ name: 'GroupView'}">小组</router-link>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'he-nav'
  }
</script>

<style scoped lang="scss" >
  .he-nav {

    ul {
      list-style: none;
      overflow: hidden;
      margin: 1rem 0 0 0;
      padding-top: 0.6rem;

      li {
        float: left;
        width: 50%;
        padding: 1.2rem;
        box-sizing: border-box;
        font-size: 1.5rem;
        text-align: center;
      }
      a{
        display: block;
      }
    }
  }


</style>
