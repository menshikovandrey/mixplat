<template>
  <div>
    <div id="subscriptionsNone" class="row">
      <div class="col-lg-6 mx-auto">
        <div class="error">Подписки не найдены. Проверьте данные и попробуйте еще раз</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SubscriptionsNone'
}
</script>

<style scoped>
#subscriptionsNone {
  display: none;
  margin-top: 30px;
}
.error {
  color: #F44356;
}
</style>
