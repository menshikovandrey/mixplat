<template>
  <div>

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
              <td>*7777</td>
              <td>575</td>
              <td class="icons_subscriptions">
                <img src="../assets/images/icon_edit.png" alt="Настроить подписку" class="icon_edit">
                <img src="../assets/images/icon_delete.png" alt="Отменить подписку" class="icon_delete">
              </td>
            </tr>
            <tr>
              <td>*9666</td>
              <td>200</td>
              <td class="icons_subscriptions">
                <img src="../assets/images/icon_edit.png" alt="Настроить подписку" class="icon_edit">
                <img src="../assets/images/icon_delete.png" alt="Отменить подписку" class="icon_delete">
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
  name: 'Subscriptions'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
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

/*table.table-subscriptions thead tr td,
table.table-subscriptions tbody tr td {
  width: 33% !important;
}*/

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

.icon_edit,
.icon_delete {
  margin-left: 20px;
}

.icons_subscriptions {
  text-align: right !important;
}
</style>
