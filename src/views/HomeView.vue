<template>
  <div class="home-view">
    <he-nav></he-nav>
    <list mold="thumbnail" :items="events"></list>
    <infinite-loading @infinite="onInfinite" ref="infiniteLoading">    </infinite-loading>
  </div>
</template>

<script>
  import HeNav from '../components/HeNav.vue'
  import List from '../components/List.vue'
  import InfiniteLoading from 'vue-infinite-loading'
  import { mapState, mapActions } from 'vuex'

  export default {
    name: 'home-view',
    components: { HeNav, List, InfiniteLoading},
    data (){
      return {

      }
    },
    computed: {
      // Getting Vuex State from store/modules/activities
      ...mapState({
        events: state => state.activities.events
      })
    },
    methods: {
      // Using vue-infinite-loading
      onInfinite() {
        setTimeout(() => {
          this.loadMore()
          this.$refs.infiniteLoading.stateChanger.loaded()
        }, 10000);
      },
      ...mapActions([
        'loadMore', // 将 `this.loadMore()` 映射为 `this.$store.dispatch('loadMore')`
      ])
    }
  }
</script>

<style scoped=""></style>
