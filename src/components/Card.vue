<template>
  <div>
    <div id="formCardContainer" class="row">
      <div class="col-lg-5 mx-auto">
        <div class="card">
          <div class="card-body">
            <form id="formCard" action="#">

              <div class="form-group row">
                <label class="col-lg-3 col-form-label">Способ оплаты</label>
                <div class="col-lg-9">
                  <select id="method" name="method" class="custom-select">
                    <option value="card">Банковская карта</option>
                    <option value="mobile">С баланса мобильного</option>
                    <option value="apple">Apple Pay</option>
                  </select>
                </div>
              </div>

              <div class="form-group row">
                <label class="col-lg-3 col-form-label">Номер карты</label>
                <div class="col-lg-4">
                  <input
                      type="text"
                      v-mask="'9999 99'"
                      class="form-control">
                  <div class="sublabel">Первые 6 цифр</div>
                </div>
                <div class="col-lg-1"></div>
                <div class="col-lg-4">
                  <input
                      type="text"
                      v-mask="'9999'"
                      class="form-control">
                  <div class="sublabel">Последние 4 цифры</div>
                </div>
              </div>

              <div class="form-group row">
                <label class="col-lg-3 col-form-label">Месяц/год</label>
                <div class="col-lg-4">
                  <input
                      type="text"
                      v-mask="'99/99'"
                      class="form-control">
                </div>
              </div>

              <div class="form-group row">
                <label class="col-lg-3 col-form-label">Сумма</label>
                <div class="col-lg-9">
                  <input
                      type="text"
                      v-mask="'9{1,}.|,99'"
                      class="form-control">
                </div>
              </div>

              <div class="text-right">
                <button type="submit" class="btn btn-primary">Найти подписки</button>
              </div>

            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  // props: {
  // }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#formCardContainer {
  margin-top: 30px;
}

.card {
  background-color: #F5F5F5;
  box-shadow: none;
  border: none;
}

.col-form-label,
.form-control,
.custom-select {
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
