<template>
  <div class="card">
    <!--    <h1>{{ msg }}</h1>-->
    <div class="subtitle">Управление подписками</div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  // props: {
  //   msg: String
  // }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "../../node_modules/typeface-roboto/index.css";
.subtitle {
  font-family: Roboto, serif; /* fixme заменить на Roboto */
}
</style>
