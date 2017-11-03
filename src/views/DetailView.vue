<template>
  <div class="detail-view has-header">
    <banner></banner>
    <template v-if="!showLoading">
        <div class="info">
          <div class="title">
            <h2>
              {{eventItem.title}}
              <span class="loc_name">{{eventItem.loc_name}}</span>
            </h2>
          </div>
          <div class="img">
            <img :src="eventItem.image" alt="">
          </div>
          <div class="time row">
            <div class="label">
              <div>时间：</div>
            </div>
            <div class="con">
              <div>{{eventItem.begin_time}}</div>
              <div>{{eventItem.end_time}}</div>
            </div>
          </div>
          <div class="row">
            <div class="label">
              <div>地点：</div>
            </div>
            <div class="con">
              <div>{{eventItem.address}}</div>
            </div>
          </div>
          <div class="row">
            <div class="label">
              <div>费用：</div>
            </div>
            <div class="con">
              <div>{{eventItem.participant_count}}</div>
            </div>
          </div>
          <div class="row">
            <div class="label">
              <div>类型：</div>
            </div>
            <div class="con">
              <div>{{eventItem.category_name}}</div>
            </div>
          </div>
        </div>
    </template>
  </div>
</template>

<script>
  import Banner from '../components/Banner.vue'
  import { mapState, mapActions } from 'vuex'

  export default {
    name: 'detail-view',
    components: { Banner },
    data () {
      return {
        showLoading: true
      }
    },
    computed: {
      ...mapState({
        eventItem: state => state.activities.eventItem
      })
    },
    methods: {
      ...mapActions([
        'getSingleEvent', // 将 `this.loadMore()` 映射为 `this.$store.dispatch('loadMore')`
      ])
    },
    created () {
      // Getting route params
      const id = this.$route.params.id

      // Dispatching getSingleEvent
      this.$store.dispatch({
        type: 'getSingleEvent',
        id: id
      }).then(res => {
        // Success handle
        this.showLoading = false
      })
    }

  }
</script>

<style scoped="">
  .info{
    padding: 1rem;
    font-size: 1.4rem;
  }
  .title{
    /*display: flex;*/
    justify-content: flex-start;
    align-items: center;
    font-size: 1.2rem;
    overflow: hidden;
  }
  .loc_name{
    padding: 0.3rem;
    margin-left: 0.5rem;
    background-color: palevioletred;
    border-radius: 0.3rem;
    color: #fff;
    font-size: 1.2rem;
    vertical-align: middle;
  }
  .img{
    display: flex;
    justify-content: center;
  }
  .row{
    display: flex;
    align-items: flex-start;
    margin: 2rem 0;
    /*flex: 1;*/
  }
  .label{
    width: 4rem;
  }
  .con{
    flex: 1;
  }
</style>
