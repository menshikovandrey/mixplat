<template>
  <div>
    <img alt="MIXPLAT" id="logo" src="@/assets/images/logo.png"> <!-- логотип -->
    <h2>Управление подписками</h2>
    <div class="col-lg-6 mx-auto">
      <div class="info">Настройте ваши ежемесячные платежи, оформленные через платёжный сервис MIXPLAT.<br>
        На этой странице вы можете управлять своими подписками — изменить сумму дальнейших регулярных пожертвований или
        отменить их.
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
#logo {
  width: 102px;
  margin-top: 60px;
}

h2 {
  font-family: 'Roboto', sans-serif;
  font-weight: bold;
  font-size: 19px;
  line-height: 22px;
  color: #333333;
  margin: 50px 0px 0px 0px;
  text-align: center;
}

.info {
  /*width: 609px;*/
  margin: auto;
  margin-top: 10px;
  font-family: Open Sans;
  font-style: normal;
  font-weight: normal;
  font-size: 13px;
  line-height: 18px;
  text-align: center;
  color: #999999;
}
</style>
