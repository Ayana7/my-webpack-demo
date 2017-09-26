<template>
  <div class="list">
      <div class="content">
        <div class="item">
          <img src="../assets/book_zw.jpg" alt="">
          <h3>爱情究竟是谎言编织的美梦，还是真实的存在？</h3>
          <p>甜蜜的美梦和残酷的现实，你会选择哪一个？小说虚构出“爱情剧本”软件，借由离奇荒诞的情节来探讨爱情的本质。</p>
          <div class="author">by&nbsp;<span class="name">豆瓣</span></div>
          <span class="feed-label">来自栏目 广播精选</span>
        </div>
        <div class="item">
          <img src="../assets/book_zw.jpg" alt="">
          <h3>爱情究竟是谎言编织的美梦，还是真实的存在？</h3>
          <p>甜蜜的美梦和残酷的现实，你会选择哪一个？小说虚构出“爱情剧本”软件，借由离奇荒诞的情节来探讨爱情的本质。</p>
        </div>
      </div>
  </div>
</template>

<script>
  export default {
    name: 'list'
  }
</script>

<style scoped lang="scss">
  .list{
    .item{
      position: relative;
      overflow: hidden;
      font-size: 1.6rem;
      padding: 1.8rem;
      img{
        width: 25%;
        float: right;
        padding-left: 1rem;
        position: relative;
      }
      h3{
        text-align: justify;
        font-size: 17px;
        font-weight: 500;
        line-height: 1.41;
        color: #494949;
        margin: 6px 0;
      }
      p{
        text-align: justify;
        color: #aaa;
        font-size: 12px;
        line-height: 1.5;
        display: -webkit-box;
        overflow: hidden;
        -webkit-box-orient: vertical;
        -webkit-line-clamp: 3;
      }
      .author{
        font-size: 12px;
        color: #aaa;
      }
      .feed-label{
        position: absolute;
        bottom: 20px;
        right: 20px;
        font-size: 12px;
        color: #ccc;
      }
    }
  }
</style>
