<template>
  <div id="app">

    <Header/> <!-- Заголовок -->

    <!-- Выпадающий список -->
    <div id="selectContainer" class="row">
      <div class="col-lg-4 mx-auto">
        <div class="form-group row">
          <label class="col-lg-4 col-form-label">Способ оплаты</label>
          <div class="col-lg-8">
            <select v-model="selected"
                    @change="onChange()"
                    class="custom-select form-control">
              <option v-for="option in this.selectOptions" v-bind:key="option.value" v-bind:value="option.value">
                {{ option.text }}
              </option>
            </select>
          </div>
        </div>
      </div>
    </div>

    <Card/>           <!-- Банковская карта -->
    <Mobile/>         <!-- С баланса мобильного -->
    <Apple/>          <!-- Apple Pay -->

    <Subscriptions/>  <!-- Подписки -->

    <Footer/>         <!-- Copyright снизу -->
  </div>
</template>

<script>
import Header from "./components/Header";
import Card from './components/Card';
import Mobile from "./components/Mobile";
import Apple from "./components/Apple";
import Subscriptions from "./components/Subscriptions";
import Footer from "./components/Footer";

export default {
  name: 'App',
  components: {Header, Card, Mobile, Apple, Subscriptions, Footer},
  data() {
    return {
      selected: 'card', // Выпадающий список - значение по умолчанию
      selectOptions: [  // Выпадающий список - массив
        {value: 'card', text: 'Банковская карта'},
        {value: 'mobile', text: 'С баланса мобильного'},
        {value: 'apple', text: 'Apple Pay'},
      ],
    }
  },
  methods: {
    /**
     * Скрыть и обнулить все компоненты и поля
     */
    eraseAllData() {
      document.getElementById('card').style.display = "none";           // скрыть Карта
      document.getElementById('mobile').style.display = "none";         // скрыть Мобильный
      document.getElementById('apple').style.display = "none";          // скрыть Apple
      document.getElementById('subscriptions').style.display = "none";  // скрыть Подписки
    },
    /**
     * Выполняется при изменеии значения в выпадабщем списке
     */
    onChange() {
      let selected = this.selected; // получаем способ оплаты
      this.eraseAllData();       // скрыть и обнулить все компоненты и поля
      switch (selected) {           // отобразить выбранный из выпадающего списка
        case 'card':
          document.getElementById('card').style.display = "flex";
          break;
        case 'mobile':
          document.getElementById('mobile').style.display = "flex";
          break;
        case 'apple':
          document.getElementById('apple').style.display = "flex";
          break;
      }
    },
  }
}
</script>

<style>
/*@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@700&display=');*/
/*@import url('https://fonts.googleapis.com/css2?family=Open+Sans&display=swap');*/
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400&family=Roboto:wght@100;300;400&display=swap');
@import './assets/icons/icomoon/styles.min.css';
@import './assets/css/all.min.css';

#app {
  text-align: center;
  overflow-y: scroll;
  overflow-x: hidden;
  min-height: 100%;
  position: relative;
}

#selectContainer {
  margin-top: 30px;
}

.col-form-label,
.custom-select {
  text-align: left;
  font-family: Open Sans;
  font-style: normal;
  font-weight: normal;
  font-size: 13px;
  color: #333333;
}
</style>
