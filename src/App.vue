<template>
  <div id="app">

    <Header/> <!-- Заголовок -->

    <!-- Выпадающий список -->
    <div id="selectContainer" class="row">
      <div class="col-lg-4 mx-auto">
        <div class="form-group row">
          <label class="col-lg-4 col-form-label">Способ оплаты</label>
          <div class="col-lg-8">
            <select
                v-model="selected"
                @change="onChange()"
                class="custom-select form-control">
              <option
                  v-for="option in this.selectOptions"
                  v-bind:key="option.value"
                  v-bind:value="option.value">
                {{ option.text }}
              </option>
            </select>
          </div>
        </div>
      </div>
    </div>

    <Card/>               <!-- Банковская карта -->
    <Mobile/>             <!-- С баланса мобильного -->
    <Apple/>              <!-- Apple Pay -->

    <Subscriptions/>      <!-- Подписки -->
    <SubscriptionsNone/>  <!-- Подписки не найдены -->

    <Footer/>             <!-- Copyright снизу -->
  </div>
</template>

<script>
import Header from "./components/Header";
import Card from './components/Card';
import Mobile from "./components/Mobile";
import Apple from "./components/Apple";
import Subscriptions from "./components/Subscriptions";
import SubscriptionsNone from "./components/SubscriptionsNone";
import Footer from "./components/Footer";

import axios from "axios";

export default {
  name: 'App',
  components: {Header, Card, Mobile, Apple, Subscriptions, SubscriptionsNone, Footer},
  data() {
    return {
      selected: 'card', // Выпадающий список - значение по умолчанию
      selectOptions: [  // Выпадающий список - массив
        {value: 'card', text: 'Банковская карта'},
        {value: 'mobile', text: 'С баланса мобильного'},
        {value: 'apple', text: 'Apple Pay'},
      ],
      subscriptions: null,
      apiSubscriptions: 'https://my-json-server.typicode.com/menshikovandrey/mixplat/subscriptions/',            // ручка подписки
      apiSubscriptionsNone: 'https://my-json-server.typicode.com/menshikovandrey/mixplat/subscriptions_none/',  // ручка пустой массив
    }
  },
  methods: {
    /**
     * Скрыть компоненты и обнулить поля
     */
    eraseAllData() {
      /*
      Скрываем все экраны по умолчанию
       */
      let screens = document.getElementsByClassName("screen");
      console.log(screens)
      for (let i = 0; i < screens.length; i++)
        screens[i].style.display = "none";

      /*
      Задаем пустое значение для всех полей input
       */
      let fields = document.getElementsByTagName("input");
      console.log(fields)
      for (let j = 0; j < fields.length; j++)
        fields[j].value = "";
    },
    /**
     * Выполняется при изменеии значения в выпадабщем списке
     */
    onChange() {
      let selected = this.selected; // получаем способ оплаты
      this.eraseAllData();          // скрыть и обнулить все компоненты и поля
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
    /**
     * Найти подписки (успех)
     */
    getSubscriptions() {
      axios.get(this.apiSubscriptions)
          .then(response => {
            let subscriptions = response.data;
            console.log(subscriptions);
          })
          .catch(error => {
            console.log(error);
          })
    },
    /**
     * Подписки не найдены
     */
    getSubscriptionsNone() {
      axios.get(this.apiSubscriptionsNone)
          .then(response => {
            let subscriptions = response.data;
            console.log(subscriptions);
          })
          .catch(error => {
            console.log(error);
          })
    }
  }
}
</script>

<style>
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
