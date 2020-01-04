<template>
  <div>
    <div class="card">
      <a target="_blank" rel="noopener noreferrer" :href="this.href">
        <img class="img" :src="getImgUrl(this.title)" :alt="this.title" />
      </a>
      <h5 class="title">{{ title }}</h5>
      <h6 class="Detail">{{ detail }}</h6>
    </div>
  </div>
</template>

<script>
export default {
  name: "Portfolio-card",
  props: {
    href: String,
    title: String,
    detail: String
  },
  methods: {
    getImgUrl(img) {
      return require("../assets/images/portfolio/" + img + ".png");
    }
  }
};
</script>

<style scoped lang="scss">
.card {
  background-color: #fffffffd;
  border-radius: 10px;
  box-shadow: 0px 0px 10px 2px rgba(173, 173, 173, 0.596);
  .img {
    border-radius: 10px;
    width: 100%;
    padding-bottom: 40px;
  }
  .title {
    padding-bottom: 10px;
    font-size: 25px;
    font-weight: bold;
  }
  .Detail {
    font-size: 17px;
    padding-bottom: 50px;
  }
}
@media (max-width: 893px) {
}
</style>
