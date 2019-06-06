<template>
  <div class="panel">
    <h2>{{ panelTit }}</h2>
    <div :id="panelId" style="width: 100%; height: 100%;"></div>
  </div>
</template>

<script>
let echarts = require("echarts/lib/echarts");
require("echarts/lib/chart/gauge");
require("echarts/lib/component/title");
require("echarts/lib/component/tooltip");

export default {
  name: "panel",
  props: {
    panelTit: String,
    panelId: String
  },
  mounted() {
    this.drawLine();
  },
  methods: {
    drawLine() {
      let pChart = echarts.init(document.getElementById(this.panelId));

      pChart.setOption({
        tooltip: {
          formatter: "{a} <br/>{b} : {c}%"
        },
        series: [
          {
            name: "实时一次合格率",
            type: "gauge",
            radius: "60%",
            splitNumber: 5,
            splitLine: {
              show: false
            },
            axisTick: {
              splitNumber: 10,
              length: 3
            },
            axisLine: {
              lineStyle: {
                width: 10
              }
            },
            axisLabel: {
              distance: -15,
              fontSize: 10
            },
            pointer: {
              width: 3
            },
            detail: {
              formatter: "{value}%",
              color: "#fff",
              fontSize: 10
            },
            data: [{ value: 100 }]
          }
        ]
      });
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.panel {
  background: url("../assets/main_bs.png") no-repeat center;
  background-size: 100% 100%;
}
.panel h2 {
  width: 100%;
  position: absolute;
  top: 0;
  text-align: center;
  line-height: 3rem;
  font-size: 0.8rem;
}
</style>
