<template>
  <!--vuejs-calendar-component-header-->
  <!--@author: 梁凤波-->
  <!--@date  2018/10/15 10:01-->
  <section class="vuejs-calendar-component-header-wrap">
    <header class="vuejs-calendar-component-header-box">
      <!--action-btn-->
      <div class="calendar-action">
        <button class="calendar-action-btn calendar-action-btn-1"></button>
      </div>

      <!--year-->
      <div class="calendar-header-item calendar-year">
        <select class="calendar-header-item-select calendar-year-select">
          <option value="2018">2018年</option>
          <option value="2019">2019年</option>
          <option value="2020">2020年</option>
          <option value="2021">2021年</option>
        </select>
      </div>

      <!--month-->
      <div class="calendar-header-item calendar-month">
        <select class="calendar-header-item-select calendar-mouth-select">
          <option value="9">9月</option>
          <option value="10">10月</option>
          <option value="11">11月</option>
          <option value="12">12月</option>
        </select>
      </div>

      <!--action-btn-->
      <div class="calendar-action">
        <button class="calendar-action-btn calendar-action-btn-2"></button>
      </div>
    </header>
  </section>
</template>

<script>
  export default {
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

<style lang="scss" scoped>
  /*box*/
  .vuejs-calendar-component-header-box {
    display: flex;
    padding: 0 32px;
    height: 96px;
    line-height: 96px;
    border-bottom: 1px solid #eee;
  }

  .calendar-header-item {
    flex: 1;
    color: #434343;
    text-align: center;
  }

  /*select*/
  .calendar-header-item-select {
    border: none;
    outline: none;
    font-size: 36px;
    background: #fff;
    margin: 0;
    padding: 0;
    color: #434343;
    text-align: center;
    text-align-last: center;
  }

  .calendar-year {
    position: relative;
  }

  .calendar-year:after {
    position: absolute;
    content: "";
    right: 0;
    top: 32px;
    width: 1px;
    height: 32px;
    background: #eee;
  }

  /*action btn*/
  .calendar-action {
    position: relative;
    padding: 0 32px;
  }

  .calendar-action-btn {
    width: 24px;
    height: 24px;
    content: "";
    border: none;
    outline: none;
    border-top: 1px solid #989898;
    border-right: 1px solid #989898;
    transform: rotate(45deg);
    background: #fff;
  }

  .calendar-action-btn-1 {
    transform: rotate(225deg);
  }
</style>
