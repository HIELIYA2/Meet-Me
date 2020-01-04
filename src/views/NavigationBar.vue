<template>
  <section>
    <div v-bind:class="{ navTop: navbarActive }" class="nav">
      <div class="logo" @click="scrollTop()">Meet Me</div>
      <div class="nav-active">
        <a class="portfolio-link link" @click="scrollPortolio()">portfolio</a>
        <a class="specialities-link link" @click="scrollSpecialities()">specialities</a>
        <a class="Me-link link" @click="scrollMe()">me</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "navigation-bar",
  props: {
    msg: String
  },
  data() {
    return {
      navbarActive: true
    };
  },
  methods: {
    scrollPortolio() {
      window.scrollTo({
        top: 737,
        behavior: "smooth"
      });
    },
    scrollSpecialities() {
      window.scrollTo({
        top: 1400,
        behavior: "smooth"
      });
    },
    scrollMe() {
      window.scrollTo({
        top: 2100,
        behavior: "smooth"
      });
    },
    scrollTop() {
      window.scrollTo({
        top: 0,
        behavior: "smooth"
      });
    },
    handleScroll(event) {
      window.pageYOffset > 80
        ? (this.navbarActive = false)
        : (this.navbarActive = true);
    }
  },
  created() {
    window.addEventListener("scroll", this.handleScroll);
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  }
};
</script>

<style lang="scss">
.nav {
  padding: 0px 0;
  z-index: 10;
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  width: 100vw;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-around;
  background: #242424e3;
  transition: all 0.4s;
  .logo {
    padding-top: 20px;
    font-family: Zeyada-Regular;
    font-size: 40px;
    color: rgb(226, 196, 27);
    cursor: pointer;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .nav-active {
    .link {
      letter-spacing: 4px;
      font-family: PoiretOne-Regular;
      margin-left: 20px;
      color: #fff;
      cursor: pointer;
      transition: 0.3s;
    }
    .link:hover {
      color: rgb(226, 196, 27);
    }
  }
}
.navTop {
  padding: 20px 0;
  background: #35353500;
  transition: 0.4s;
}

@media (max-width: 893px) {
  .nav {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    .nav-active {
      display: none;
    }
  }
}
</style>
