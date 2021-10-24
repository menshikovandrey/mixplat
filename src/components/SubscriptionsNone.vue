<template>
  <div>
    <div id="subscriptions_none" class="row">
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
#subscriptions_none {
  display: none;
  margin-top: 30px;
}
.error {
  color: #F44356;
}
</style>
