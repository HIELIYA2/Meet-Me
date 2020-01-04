<template>
  <div class="head">
    <h1 class="title-1">Welcome To my Portfolio</h1>
    <h2 class="title-2">IT'S NICE TO MEET YOU</h2>
    <button class="btn-more" @click="scrollPortolio()">tell me more</button>
  </div>
</template>

<script>
export default {
  name: "Head",
  props: {
    msg: String
  },
  methods: {
    scrollPortolio() {
      window.scrollTo({
        top: 737,
        behavior: "smooth"
      });
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.head {
  background-image: url(../assets/images/header-bg.jpg);
  background-repeat: no-repeat;
  background-attachment: scroll;
  background-position: center center;
  background-size: cover;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  padding-top: 250px;
  padding-bottom: 250px;
  .title-1 {
    color: white;
    font-family: FingerPaint-Regular, "Gill Sans", "Gill Sans MT",
      "Trebuchet MS";
    font-size: 35px;
    letter-spacing: 1px;
    margin-bottom: 45px;
  }
  .title-2 {
    color: white;
    font-size: 60px;
    letter-spacing: 3px;
    margin-bottom: 45px;
    font-weight: bold;
  }
  .btn-more {
    letter-spacing: 3px;
    font-size: 16px;
    font-family: Acme-Regular, "Gill Sans", "Gill Sans MT", sans-serif;
    padding: 16px 22px;
    border: 0;
    border-radius: 8px;
    cursor: pointer;
    font-weight: bold;
    transition: 0.3s;
    background: rgb(226, 196, 27);
  }
}

@media (max-width: 893px) {
  .head {
    .title-1 {
      color: white;
      font-family: FingerPaint-Regular, "Gill Sans", "Gill Sans MT",
        "Trebuchet MS";
      font-size: 20px;
      letter-spacing: 1px;
      margin: 0 10px 45px 10px;
    }
    .title-2 {
      color: white;
      font-size: 30px;
      letter-spacing: 3px;
      margin: 0 10px 70px 10px;
    }
  }
}
</style>
