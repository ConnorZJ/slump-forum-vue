<template>
  <div id="app">
    <img src="./assets/logo.png" />
    <router-view />
    <el-button type="primary" size="default" @click="loadTopic()">Rqeuest</el-button>
  </div>
</template>

<script>
export default {
  name: "App",
  methods: {
    loadTopic() {
      this.axios.get('/topic').then(res=>console.log(res));
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
