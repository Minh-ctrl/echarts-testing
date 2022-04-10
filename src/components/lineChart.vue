<template>
  <div class="page-line-chart">
    <VChart class="chart" :chartData="chartData"></VChart>
    <div>this running?</div>
  </div>
</template>
 
<script>
import { use } from "echarts/core";
import { CanvasRenderer } from "echarts/renderers";
import { BarChart } from "echarts/charts";
import VChart, { THEME_KEY } from "vue-echarts";
import { ref, defineComponent } from "vue";
use([
  CanvasRenderer,
  BarChart,
]);
export default defineComponent({
    components:{
        VChart
    },
      provide: {
    [THEME_KEY]: "light"
  },
    setup(){
       const  chartData = ref({
    xAxis: {
        type: 'category',
        data: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun']},
        yAxis: {type: 'value'},
        series: [
            {
                data: [120, 200, 150, 80, 70, 110, 130],
                type: 'bar',
                showBackground: true,
                backgroundStyle: {
                    color: 'rgba(180, 180, 180, 0.2)'
                    }
                }
            ]
            })
                return {chartData} 
        }
})
</script>

<style scoped>
    .chart{
        height: 600px;
        width: 600px;
}
</style>
