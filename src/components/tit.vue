<template>
  <div class="tit">
    <div class="titTop">
      <h1>智能制造企业云图</h1>
      <p>Monitoring Center</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "tit",
  props: {}
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.tit {
  padding: 0.7rem;
}
.titTop {
  width: 56%;
  margin: 0 auto;
  background: url("../assets/tit.png") no-repeat center;
  background-size: 100% 100%;
  text-align: center;
  font-size: 1rem;
  line-height: 1.5rem;
  padding-top: 0.5rem;
}
.titTop h1 {
  font-size: 1rem;
  font-weight: normal;
}
.titTop p {
  color: #4ec2ca;
}
</style>
