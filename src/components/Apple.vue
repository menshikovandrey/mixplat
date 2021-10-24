<template>
  <div>

    <div id="apple" class="row">

      <div class="col-lg-4 mx-auto">

        <div class="form-group row">
          <label class="col-lg-4 col-form-label">Номер карты</label>
          <div class="col-lg-4">
            <input
                id="apple_num_4"
                v-mask="'9999'"
                type="text"
                class="form-control"
                placeholder="0000">
            <div class="sublabel">Последние 4 цифры</div>
          </div>
        </div>

        <div class="form-group row">
          <label class="col-lg-4 col-form-label">Сумма</label>
          <div class="col-lg-8">
            <input
                id="apple_sum"
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
  name: 'Apple',
  methods: {
    onBtnClick() {
      document.getElementById('subscriptions_none').style.display = "flex";  // открыть Подписки
    },
  }
}
</script>

<style scoped>
#apple {
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

.sublabel {
  font-family: Open Sans;
  font-style: normal;
  font-weight: normal;
  font-size: 11px;
  line-height: 15px;
  display: flex;
  color: #999999;
}

.btn {
  font-family: Open Sans;
  font-style: normal;
  font-weight: normal;
  width: 100%;
}
</style>
