<template>
  <div class="lineChart">
    <div class="leftLine">
      <h2>中国区端到端及时交付率</h2>
      <div id="leftLine" style="width: 100%; height: 100%;"></div>
    </div>
    <div class="rightLine">
      <h2>周单板和整机一次合格率</h2>
      <div id="rightLine" style="width: 100%; height: 100%;"></div>
    </div>
  </div>
</template>

<script>
let echarts = require("echarts/lib/echarts");
require("echarts/lib/chart/line");
require("echarts/lib/component/title");
require("echarts/lib/component/tooltip");

export default {
  name: "lineChart",
  props: {},
  mounted() {
    this.drawLine();
  },
  methods: {
    drawLine() {
      let lChart = echarts.init(document.getElementById("leftLine"));
      let rChart = echarts.init(document.getElementById("rightLine"));

      lChart.setOption({
        xAxis: {
          type: "category",
          boundaryGap: false,
          data: ["Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"]
        },
        yAxis: {
          type: "value"
        },
        series: [
          {
            data: [820, 932, 901, 934, 1290, 1330, 1320],
            type: "line",
            areaStyle: {}
          }
        ]
      });
      rChart.setOption({
        xAxis: {
          type: "category",
          boundaryGap: false,
          data: ["Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"]
        },
        yAxis: {
          type: "value"
        },
        series: [
          {
            data: [820, 932, 901, 934, 1290, 1330, 1320],
            type: "line",
            areaStyle: {}
          }
        ]
      });
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.lineChart {
  background: url("../assets/main_bc.png") no-repeat center;
  background-size: 100% 100%;
}
.leftLine {
  width: 50%;
  height: 100%;
  position: absolute;
  left: 0;
  top: 2rem;
}
.rightLine {
  width: 50%;
  height: 100%;
  position: absolute;
  right: 0;
  top: 2rem;
}
.lineChart h2 {
  width: 100%;
  position: absolute;
  top: 0;
  text-align: center;
  line-height: 3rem;
  font-size: 1rem;
  color: #4ec2ca;
}
</style>
