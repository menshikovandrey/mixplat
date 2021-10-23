<template>
  <div>

    <form action="#">

      <div id="card" class="row">

        <div class="col-lg-4 mx-auto">

          <div class="form-group row">
            <label class="col-lg-4 col-form-label">Номер карты</label>
            <div class="col-lg-4">
              <input
                  v-mask="'9999 99'"
                  type="text"
                  class="form-control">
              <div class="sublabel">Первые 6 цифр</div>
            </div>
            <div class="col-lg-4">
              <input
                  v-mask="'9999'"
                  type="text"
                  class="form-control">
              <div class="sublabel">Последние 4 цифры</div>
            </div>
          </div>

          <div class="form-group row">
            <label class="col-lg-4 col-form-label">Месяц/год</label>
            <div class="col-lg-4">
              <input
                  v-mask="'99/99'"
                  type="text"
                  class="form-control">
            </div>
          </div>

          <div class="form-group row">
            <label class="col-lg-4 col-form-label">Сумма</label>
            <div class="col-lg-8">
              <input
                  v-mask="'9{1,}.|,99'"
                  type="text"
                  class="form-control">
            </div>
          </div>

          <div class="text-right">
            <button type="submit" class="btn btn-primary">Найти подписки</button>
          </div>

        </div>

      </div>

    </form>

  </div>
</template>

<script>
export default {
  name: 'Card'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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
