<template>
  <div class="portfolio">
    <h1 class="title">Portfolio</h1>
    <h2 class="subtitle">Some of the projects I did</h2>
    <div class="cards">
      <section v-for="card in cards" v-bind:key="card.title">
        <div class="card-container">
          <portfolioCard
            class="portfolio-card"
            :title="card.title"
            :detail="card.detail"
            :href="card.href"
          />
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import portfolioCard from "./Portfolio-card.vue";

export default {
  name: "Portfolio",
  props: {},
  components: {
    portfolioCard
  },
  data() {
    return {
      cards: [
        {
          title: "bestask",
          detail: "Project management app",
          href: "https://bestaskmanager.herokuapp.com"
        },
        {
          title: "meme",
          detail: "Meme jenerator",
          href: "https://hieliya2.github.io/meme-generator/"
        },
        {
          title: "appsus",
          detail: "App that combines mail and notes",
          href: "https://hieliya2.github.io/sprint-3"
        },
        {
          title: "borsood (W.I.P)",
          detail: "תוכנה לשינון מונחים ",
          href: "https://borsood.herokuapp.com/"
        },
        {
          title: "get-bus  (W.I.P)",
          detail: "Customer and supplier transportation order management system",
          href: "https://get-bus.herokuapp.com/"
        }
      ]
    };
  }
};
</script>

<style scoped lang="scss">
.portfolio {
  padding-top: 100px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;
  height: auto;
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
  .cards {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    align-items: stretch;
    .card-container {
      width: 40vw;
      max-width: 400px;
      margin: 15px;
      .portfolio-card {
        width: 100%;
      }
    }
  }
}
@media (max-width: 893px) {
  .portfolio {
    padding-top: 100px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-content: center;
    height: auto;
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
    .cards {
      display: flex;
      flex-flow: row wrap;
      justify-content: center;
      align-items: center;
      .card-container {
        width: 45vw;
        min-width: 300px;
        .portfolio-card {
          width: 100%;
        }
      }
    }
  }
}
</style>
