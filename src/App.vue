<template>
  <div id="app">
    <JastipDashboard />
  </div>
</template>

<script>
import JastipDashboard from './components/JastipDashboard.vue';

export default {
  name: 'App',
  components: {
    JastipDashboard,
  },
};
</script>

<style>
body {
  background-color: skyblue;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>