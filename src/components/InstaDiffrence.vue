<template>
  <div class="border">
    <vue-highcharts :options="options" ref="pieCharts"></vue-highcharts>
      <Table/>
  </div>
</template>
 
<script>
import VueHighcharts from 'vue2-highcharts';
import Table from './Table'
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
            text: 'Instagram Diffrence'
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
            name: 'Diffrence',
            data: [
              ['Male', 10],
              ['Female', 3],
              ['Others', 1]
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