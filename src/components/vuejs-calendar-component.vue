<template>
  <!--vuejs-calendar-component-->
  <!--@author: 梁凤波-->
  <!--@date  2018/10/15 09:40-->
  <section class="vuejs-calendar-component-wrap">
    <!--box-->
    <article class="vuejs-calendar-component-box">
      <!--header-->
      <VuejsCalendarComponentHeader/>
      <!--date-->
      <VuejsCalendarComponentDate/>
    </article>
  </section>
</template>

<script>
  import VuejsCalendarComponentHeader from './vuejs-calendar-component-header'
  import VuejsCalendarComponentDate from './vuejs-calendar-component-date'

  export default {
    components: {
      VuejsCalendarComponentHeader,
      VuejsCalendarComponentDate
    },
    data() {
      return {}
    },
    computed: {},
    created() {
    },
    methods: {}
  }
</script>

<style scoped>
  .vuejs-calendar-component-wrap {
    max-width: 750px;
    min-width: 750px;
  }
</style>
