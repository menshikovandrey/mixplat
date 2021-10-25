<template>
  <div>

    <b-modal
        size="sm"
        id="modal_edit"
        centered
        title="Настройка подписки">
      <div class="d-block text-center">
        <div class="form-group row">
          <label class="col-lg-4 col-form-label">Сумма</label>
          <div class="col-lg-8">
            <input
                id="modal_edit_sum"
                v-mask="'9{1,}.|,99'"
                type="text"
                class="form-control"
                placeholder="000.00">
          </div>
        </div>
      </div>
    </b-modal>

    <b-modal
        size="sm"
        id="modal_delete"
        centered
        title="Отмена подписки">
      <div class="d-block">
        Подписка будет отменена. Вы уверены?
      </div>
    </b-modal>

    <b-modal
        size="sm"
        id="modal_confirm"
        centered
        title="Код подтверждения">
      <div class="d-block">
        Мы отправили код подтверждения на email meo***2@gmail.com.
        <div class="form-group row">
          <label class="col-lg-4 col-form-label">Введите код</label>
          <div class="col-lg-8">
            <input
                id="modal_confirm_code"
                v-mask="'999999'"
                type="text"
                class="form-control"
                placeholder="000000">
          </div>
        </div>
      </div>
    </b-modal>

    <div id="subscriptions" class="row">

      <div class="card col-lg-6 mx-auto">

        <div class="card-header">
          <h5 class="card-title">Подписки</h5>
        </div>

        <div class="table-responsive">

          <table class="table table-borderless table-subscriptions">
            <thead class="table-header">
            <tr>
              <td>Номер карты</td>
              <td>Сумма</td>
              <td></td>
            </tr>
            </thead>
            <tbody>
            <tr>
              <td>*9666</td>
              <td>200</td>
              <td class="icons_subscriptions">
                <button
                    @click="$bvModal.show('modal_edit')"
                    type="button"
                    class="btn shadow-0 delete-cross btn-icon">
                  <i class="icon-cog" title="Настроить подписку"></i>
                </button>
                <button
                    @click="$bvModal.show('modal_delete')"
                    type="button"
                    class="btn shadow-0 text-danger delete-cross btn-icon">
                  <i class="icon-cross2" title="Отменить подписку"></i>
                </button>
              </td>
            </tr>
            </tbody>
          </table>

        </div>

      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Subscriptions',
  methods: {}
}
</script>

<style scoped>
#subscriptions {
  display: none;
  margin-top: 30px;
}

.card {
  text-align: left;
  padding-right: 0 !important;
  padding-left: 0 !important;
}

h5.card-title {
  font-family: 'Roboto', sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 17px;
  line-height: 20px;
}

.table-header {
  background: #FAFAFA !important;
}

.icons_subscriptions {
  text-align: right !important;
}
</style>
