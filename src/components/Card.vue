<template>
  <div>

    <div id="card" class="row">

      <div class="col-lg-4 mx-auto">

        <div class="form-group row">
          <label class="col-lg-4 col-form-label">Номер карты</label>
          <div class="col-lg-4">
            <input
                v-mask="'9999 99'"
                type="text"
                class="form-control"
                placeholder="0000 00">
            <div class="sublabel">Первые 6 цифр</div>
          </div>
          <div class="col-lg-4">
            <input
                v-mask="'9999'"
                type="text"
                class="form-control"
                placeholder="0000">
            <div class="sublabel">Последние 4 цифры</div>
          </div>
        </div>

        <div class="form-group row">
          <label class="col-lg-4 col-form-label">Месяц/год</label>
          <div class="col-lg-4">
            <input
                v-mask="'99/99'"
                type="text"
                class="form-control"
                placeholder="ММ/ГГ">
          </div>
        </div>

        <div class="form-group row">
          <label class="col-lg-4 col-form-label">Сумма</label>
          <div class="col-lg-8">
            <input
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
  name: 'Card',
  methods: {
    onBtnClick() {
      document.getElementById('subscriptions').style.display = "flex";  // открыть Подписки
    },
  }
}
</script>

<style scoped>
#card {
  display: flex;
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
