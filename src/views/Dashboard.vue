 <template>
  <div>
    <h1>Dashboard</h1>

    
    <div class="chart1">
      <h1>Line graph</h1>
      <apexchart
        width="500"
        type="line"
        :options="options"
        :series="series"
      ></apexchart>
     
      <div class="chart">
      <h1>Bar Graph</h1>
      <apexchart
        width="500"
        type="bar"
        :options="options"
        :series="series"
      ></apexchart>
    </div>
    </div>
  </div>
</template>

<script >
import Vue from "vue";
import VueApexCharts from "vue-apexcharts";
Vue.use(VueApexCharts);

Vue.component("apexchart", VueApexCharts);

export default {
  name: "Dashboard",
  data: function () {
    return {
      options: {
        chart: {
          id: "vuechart-example",
        },
        xaxis: {
          categories: [2010, 2011, 2015, 2017, 2018, 2019, 2020, 2021],
        },
      },
      series: [
        {
          name: "series-1",
          data: [4.5,10.5,20,30.5,50.5,45.5,55.6,90,100],
        },
      ],
    };
  },
};
</script>
<style scoped>
.chart1{
  position: absolute;
  top: 90px;
  left: 0%;
}
.chart{
  position: relative;
  left: 600px;
  /* top: 80%; */
  bottom: 360px;
}
</style>