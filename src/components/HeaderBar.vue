<template>
  <div class="header-bar">
    <h1 class="title">
      <router-link :to="{ name: 'HomeView' }">
        豆瓣
      </router-link>
    </h1>
    <ul class="nav">
      <li>
        <router-link style="color: #2384E8" :to="{ name: 'MovieView'}">电影</router-link>
      </li>
      <li>
        <router-link style="color: #2384E8" :to="{ name: 'BookView'}">图书</router-link>
      </li>
      <li>
        <router-link style="color: #2384E8" :to="{ name: 'StatusView'}">广播</router-link>
      </li>
      <li>
        <router-link style="color: #2384E8" :to="{ name: 'GroupView'}">小组</router-link>
      </li>
    </ul>
    <div class="search"></div>
  </div>
</template>

<script>
  export default {
    name: 'header-bar'
  }
</script>

<style scoped="" lang="scss">
  .header-bar{
    height: 4.7rem;
    padding: 0 1.8rem;
    box-sizing: border-box;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    position: fixed;
    top: 0;
    .title{
      flex: 1;
      width: 4.6rem;
      height: 2.2rem;
      font-size: 0;
      line-height: 3.2rem;
      color: #00b600;
      background: url("../assets/login.png") no-repeat;
      background-size: cover;
      a{
        display: block;
      }
    }
    ul{
      list-style: none;
      display: flex;
      justify-content: flex-end;
    }
    li {
      display: inline-block;
      font-size: 1.6rem;
      margin-right: 1.2rem;
    }
    .search{
      font-size: 0;
      width: 2.4rem;
      height: 1.8rem;
      margin-top: 0.4rem;
      background: url("../assets/search.png") no-repeat;
      background-size: cover;
    ;
    }
  }
</style>
