<template>
  <div class="detail">
    <h1 class="title">{{ title }}</h1>
    <h3 class="subtitle">{{ details }}</h3>
  </div>
</template>

<script>
export default {
  name: "Detail",
  props: {
    title: String,
    details: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.detail {
  display: flex;
  flex-direction: column;
  margin-bottom: 20px;
  .title {
    font-weight: bold;
  }
}
</style>
