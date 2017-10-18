<template>
  <div class="banner">
    <div class="tip">
      <p>用APP打开</p>
      <p>更多优质原创内容</p>
    </div>
    <div>
      <a href="#" class="btn1">极速下载</a>
      <a href="#" class="btn2">快速打开</a>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'banner'
  }
</script>

<style scoped="" lang="scss">
  .banner{
    width: 100%;
    height: 8rem;
    padding: 1.8rem;
    box-sizing: border-box;
    background: url("../assets/promotion_bg.jpg") no-repeat;
    background-size: cover;
    display: flex;
    justify-content: space-between;
    align-items: center;
    .tip{
      color: #2CA532;
    }
    a{
      border-radius: 5px;
      padding: 5px 10px;
      font-weight: 500;
    }
    .btn1{
      background: #2CA532;
      color: #FFF;
      border: 1px solid #2CA532;
      margin-right: 5px;
    }
    .btn2{
      border: 1px solid #2CA532;
      color: #2CA532;
    }
  }
</style>
