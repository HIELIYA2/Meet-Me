<template>
  <div class="home">
    <Head msg="Welcome to App" />
    <Portfolio />
    <Specialities />
    <Me />
  </div>
</template>

<script>
// @ is an alias to /src
import Head from "@/components/Head.vue";
import Portfolio from "../components/Portfolio.vue";
import Specialities from "../components/Specialities.vue";
import Me from "../components/Me.vue";

export default {
  name: "home",
  components: {
    Head,
    Specialities,
    Portfolio,
    Me
  }
};
</script>

<style scoped lang="scss">
.home {
  display: flex;
  flex-direction: column;
}
</style>
