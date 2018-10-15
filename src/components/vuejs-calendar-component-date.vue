<template>
  <!--vuejs-calendar-component-content-->
  <!--@author: 梁凤波-->
  <!--@date  2018/10/15 10:56-->
  <section class="vuejs-calendar-component-date-wrap">
    <div class="vuejs-calendar-component-date-box">
      <table class="calendar-date-table" v-if="date">
        <tr class="calendar-date-week-tr">
          <td class="calendar-date-week-td calendar-date-td_week">日</td>
          <td class="calendar-date-week-td">一</td>
          <td class="calendar-date-week-td">二</td>
          <td class="calendar-date-week-td">三</td>
          <td class="calendar-date-week-td">四</td>
          <td class="calendar-date-week-td">五</td>
          <td class="calendar-date-week-td calendar-date-td_week">六</td>
        </tr>
        <tr class="calendar-date-tr" v-for="(item, dateIndex) in date" :key="'item' + dateIndex">
          <td
            v-if="item.week"
            v-for="(week, index) in item.week" :key="'week' + index"
            @click="chooseDate(week.date, index)"
            :class="{'calendar-date-td_week': week.isWeek, 'calendar-date-td': true, 'calendar-date-td_active': dateActive === week.date + index,}">
            <p>{{week.date}}</p>
            <p>{{week.almanac}}</p>
          </td>
        </tr>
      </table>
    </div>
  </section>
</template>

<script>

  export default {
    data() {
      return {
        date: [
          {
            week: [
              {date: 1, almanac: "初一", isWeek: true},
              {date: 2, almanac: "初二", isWeek: false},
              {date: 3, almanac: "初三", isWeek: false},
              {date: 4, almanac: "初四", isWeek: false},
              {date: 5, almanac: "初五", isWeek: false},
              {date: 6, almanac: "初六", isWeek: false},
              {date: 7, almanac: "情人节", isWeek: true},
            ],
          },
          {
            week: [
              {date: 8, almanac: "初八", isWeek: true},
              {date: 9, almanac: "初九", isWeek: false},
              {date: 10, almanac: "十一", isWeek: false},
              {date: 11, almanac: "十二", isWeek: false},
              {date: 12, almanac: "十三", isWeek: false},
              {date: 13, almanac: "十四", isWeek: false},
              {date: 14, almanac: "十五", isWeek: true},
            ]
          }
        ],
        dateActive: -1,
      }
    },
    computed: {},
    created() {
    },
    mounted() {
    },
    methods: {
      /**
       * 点击选择日期
       * @param date 日期
       * @param index 索引
       */
      chooseDate(date, index) {
        this.dateActive = date + index;
      }
    }
  }
</script>

<style lang="scss" scoped>
  .calendar-date-table {
    width: 100%;
    box-sizing: border-box;
    padding: 0 16px;
  }

  /*星期头部*/
  .calendar-date-week-tr {
    display: flex;
    width: 100%;
  }

  .calendar-date-week-td {
    width: 14.28%;
    cursor: pointer;
    font-weight: 800;
    text-align: center;
    font-size: 34px;
    padding: 24px 0;
    color: #434343;
    border-bottom: 1px solid #f0f0f0;
  }

  /*日期列表*/
  .calendar-date-tr {
    display: flex;
    width: 100%;
    border-bottom: 1px solid #f0f0f0;
  }

  .calendar-date-td {
    cursor: pointer;
    width: 14.28%;
    height: 14.28%;
    font-size: 28px;
    padding: 16px 0;
    text-align: center;
    border: 3px solid transparent;
  }

  .calendar-date-td:hover {
    background: #fff;
  }

  .calendar-date-td_active {
    border: 3px solid #ff9900;
  }

  .calendar-date-td p {
    margin: 0;
    padding: 0;
  }

  .calendar-date-td_date {
    color: #000;
    font-size: 32px;
    font-weight: 800;
  }

  .calendar-date-td_note {
    color: #989898;
    font-size: 26px;
  }

  .calendar-date-td_week {
    color: #ed4014;
  }
</style>
