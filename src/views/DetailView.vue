<template>
  <div class="detail-view has-header">
    <banner></banner>
    <template>
        <h3>{{eventItem.title}}</h3>
    </template>
  </div>
</template>

<script>
  import Banner from '../components/Banner.vue'
  import { mapState, mapActions } from 'vuex'

  export default {
    name: 'detail-view',
    components: { Banner },
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

<style scoped=""></style>
