<template>
  <div class="home">
    <tit />
    <div class="nav">
      <router-link to="/manager">进入管理模块</router-link>
    </div>
    <div class="box">
      <info class="mainInfo" />
      <lineChart class="mainlineChart" />
      <panel
        class="mainLeftPanel"
        panelId="leftPanel"
        panelTit="单板实时一次合格率"
      />
      <panel
        class="mainRightPanel"
        panelId="rightPanel"
        panelTit="整机实时一次合格率"
      />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import tit from "@/components/tit.vue";
import info from "@/components/info.vue";
import panel from "@/components/panel.vue";
import lineChart from "@/components/lineChart.vue";

export default {
  name: "home",
  components: {
    tit,
    info,
    panel,
    lineChart
  }
};
</script>

<style scoped>
.nav {
  position: absolute;
  right: 2rem;
  top: 0.8rem;
}
.nav a {
  font-size: 0.8rem;
  color: #4ec2ca;
  text-decoration: none;
}
.box {
  width: calc(100% - 1.4rem);
  margin: -1.9rem auto;
  position: relative;
}
.mainInfo {
  width: 100%;
  height: 20.2rem;
}
.mainlineChart {
  width: 50.6%;
  height: 14rem;
  position: absolute;
  top: 19rem;
  left: 24.7%;
}
.mainLeftPanel {
  width: 24%;
  height: 14rem;
  position: absolute;
  left: 0;
  top: 19rem;
}
.mainRightPanel {
  width: 24%;
  height: 14rem;
  position: absolute;
  right: 0;
  top: 19rem;
}
</style>
