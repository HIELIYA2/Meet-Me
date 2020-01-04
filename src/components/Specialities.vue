<template>
  <div class="specialities">
    <h1 class="title">specialities</h1>
    <h2 class="subtitle">Technologies I have learned and implemented in projects</h2>
    <section class="list-specialities slide-in-right">
      <div class="specialities-" v-for="logo in logos" v-bind:key="logo">
        <Detail :title="logo" details />
        <div class="circle">
          <img class="logo" :src="getImgUrl(logo)" :alt="logo" />
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import Detail from "./Detail.vue";

export default {
  name: "Specialities",
  components: {
    Detail
  },
  props: {},
  data() {
    return {
      logos: ["vue", "react", "html", "js", "css", "sass", "git", "node", "npm"]
    };
  },
  methods: {
    getImgUrl(logo) {
      return require("../assets/images/specialities/" + logo + ".png");
    }
  }
};
</script>

<style scoped lang="scss">
.specialities {
  height: 100vh;
  margin: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;
  .title {
    font-family: Lato_bold;
    margin-bottom: 20px;
    font-size: 40px;
    text-transform: uppercase;
  }
  .subtitle {
    margin-bottom: 100px;
    font-size: 20px;
  }
  .list-specialities {
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: Lato_regular;
    .specialities- {
      margin: 0 30px;
      display: flex;
      flex-direction: column;
      align-items: center;
      .logo {
        width: 120px;
        height: 120px;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-bottom: 20px;
        .fa-laptop {
          font-size: 50px;
          color: white;
        }
      }
    }
  }
}

.slide-in-right {
  animation: slide-in-right 20s cubic-bezier(0, 0, 0, 0) both;
  animation-iteration-count: infinite;
}

@keyframes slide-in-right {
  0% {
    transform: translateX(200px);
    opacity: 1;
  }
  50% {
    transform: translateX(-200px);
    opacity: 1;
  }
  100% {
    transform: translateX(200px);
    opacity: 1;
  }
}

@media (max-width: 893px) {
  .slide-in-right {
    animation: none;
  }
  .specialities {
    height: 100vh;
    margin: 20px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    .title {
      font-family: Lato_bold;
      margin-bottom: 20px;
      font-size: 40px;
      text-transform: uppercase;
    }
    .subtitle {
      margin-bottom: 100px;
      font-size: 20px;
    }
    .list-specialities {
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      justify-content: center;
      align-items: center;
      font-family: Lato_regular;
      .specialities- {
        margin: 0 20px;
        display: flex;
        flex-direction: column;
        align-items: center;
        .logo {
          width: 50px;
          height: 50px;
          display: flex;
          justify-content: center;
          align-items: center;
          margin-bottom: 20px;
        }
      }
    }
  }
}
</style>
