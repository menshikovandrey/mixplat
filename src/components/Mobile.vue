<template>
  <div>

    <div id="mobile" class="row">

      <div class="col-lg-4 mx-auto">

        <div class="form-group row">
          <label class="col-lg-4 col-form-label">Номер телефона</label>
          <div class="col-lg-8">
            <input
                id="mobile_tel"
                v-mask="'+7 (999) 999-99-99'"
                type="text"
                class="form-control"
                placeholder="+7 (___) ___-__-__">
          </div>
        </div>

        <div class="form-group row">
          <label class="col-lg-4 col-form-label">Сумма</label>
          <div class="col-lg-8">
            <input
                id="mobile_sum"
                v-mask="'9{1,}.|,99'"
                type="text"
                class="form-control"
                placeholder="000.00">
          </div>
        </div>

        <div class="text-right">
          <button
              v-on:click="onBtnClick()"
              id="btnCard"
              type="submit"
              class="btn btn-primary">
            Найти подписки
          </button>
        </div>

      </div>

    </div>

  </div>
</template>

<script>
export default {
  name: 'Mobile',
  methods: {
    onBtnClick() {
      document.getElementById('subscriptions_none').style.display = "flex";  // открыть Подписки
    },
  }
}
</script>

<style scoped>
#mobile {
  display: none;
}

.col-form-label,
.form-control {
  text-align: left;
  font-family: Open Sans;
  font-style: normal;
  font-weight: normal;
  font-size: 13px;
  color: #333333;
}

.btn {
  font-family: Open Sans;
  font-style: normal;
  font-weight: normal;
  width: 100%;
}
</style>
