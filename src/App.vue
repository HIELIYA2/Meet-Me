<template>
  <div class="app">
    <navigation-bar msg="this is nav" />
    <router-view />
  </div>
</template>

<script>
import NavigationBar from "@/views/NavigationBar.vue";

export default {
  name: "app",
  components: {
    NavigationBar
  }
};
</script>

<style lang="scss">
.app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  font-size: 19px;
}
</style>
