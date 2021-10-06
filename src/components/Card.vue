<template>
  <div class="cardContainer">
    <h2>Управление подписками</h2>
    <div class="slogan">Настройте ваши ежемесячные платежи, оформленные через платёжный сервис MIXPLAT.<br>
      На этой странице вы можете управлять своими подписками — изменить сумму дальнейших регулярных пожертвований или
      отменить их.</div>
    <form action=""></form>
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
.cardContainer {
  text-align: center;
}

h2 {
  font-family: 'Roboto', sans-serif;
  font-weight: bold;
  font-size: 19px;
  line-height: 22px;
  color: #333333;
  margin: 60px 0px 0px 0px;
}

.slogan {
  width: 609px;
  font-family: Open Sans;
  font-style: normal;
  font-weight: normal;
  font-size: 13px;
  line-height: 18px;
  text-align: center;
  color: #999999;

  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
