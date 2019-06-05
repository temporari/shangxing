<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">进入管理模块</router-link> |
      <router-link to="/manager">进入综合监控</router-link>
    </div>
    <router-view />
  </div>
</template>

<style>
body, div, a, h1, h2, h3, h4, h5, h6, p, img {
  margin: 0;
  padding: 0;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  position: relative;
  width: 100%;
  height: 100%;
  background-color: #108ee9;
  color: #fff;
}
</style>
