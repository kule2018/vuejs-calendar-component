<template>
  <!--index-->
  <!--@author: 梁凤波-->
  <!--@date  2018/10/15 09:41-->
  <section class="index-wrap">
    <VuejsCalendarComponent/>
  </section>
</template>

<script>
  import VuejsCalendarComponent from '../components/vuejs-calendar-component'

  export default {
    components: {
      VuejsCalendarComponent
    },
    data() {
      return {}
    },
    computed: {},
    created() {
    },
    mounted() {
    },
    methods: {}
  }
</script>

<style scoped>
  .index-wrap {
    width: 100%;
    height: 100%;
  }
</style>
