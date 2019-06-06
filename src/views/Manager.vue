<template>
  <div class="manager">
    <tit />
    <div class="nav">
      <router-link to="/">进入综合监控</router-link>
    </div>
    <h2 style="text-align: center; padding-top: 50px;">
      This is an unfinished page
    </h2>
  </div>
</template>

<script>
// @ is an alias to /src
import tit from "@/components/tit.vue";

export default {
  name: "home",
  data() {
    return {};
  },
  components: {
    tit
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
</style>
