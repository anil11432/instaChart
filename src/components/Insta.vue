<template>
  <div class="border">
    <vue-highcharts :options="options" ref="pieCharts"></vue-highcharts>
    <Table/>
  </div>
</template>
 
<script>
import VueHighcharts from 'vue2-highcharts';
import Table from './Table';
export default{
    components: {
      VueHighcharts, Table
    },
    data(){
      return{
        options: {
          chart: {
            type: 'pie',
            options3d:{
              enabled: true,
              alpha: 45
            }
          },
          title: {
            text: 'Instagram followers'
          },
          subtitle: {
            // text: 'Source: WorldClimate.com'
          },
          tooltip: {
            crosshairs: true,
            shared: true
          },
          credits: {
            enabled: false
          },
          plotOptions: {
            pie: {
              innerSize: 100,
              depth: 45
            }
          },
          series: [{
            name: 'Followers',
            data: [
              ['Male', 45],
              ['Female', 32],
              ['Others', 5]
            ]
          }]
        },
      }
    },
    mounted: function () {
          let pieCharts = this.$refs.pieCharts;
    }
}
</script>

<style>
  .border{
    border: 3px solid black;
  }
</style>
