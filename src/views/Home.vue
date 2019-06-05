<template>
  <div class="home">
    <general id="mainGeneral" />
    <world id="mainWorld" />
    <china id="mainChina" />
    <lineChart id="mainLine" />
    <panel id="mainLeftPanel" />
    <panel id="mainRightPanel" />
  </div>
</template>

<script>
// @ is an alias to /src
import general from "@/components/general.vue";
import world from "@/components/world.vue";
import china from "@/components/china.vue";
import panel from "@/components/panel.vue";
import lineChart from "@/components/lineChart.vue";

export default {
  name: "home",
  components: {
    general,
    world,
    china,
    panel,
    lineChart,
  }
};
</script>

<style scoped>

</style>

