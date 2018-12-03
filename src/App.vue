<template>
  <div id="App">
    <app-header></app-header>
    <div class="user-panel">
      <div class="user-panel__fields">
        <div>
          <label>
            <span>Имя</span>
            <input type="text" v-model.trim="userName" placeholder="">
          </label>
        </div>
        <div>
          <label>
            <span>Фамилия</span>
            <input type="text" v-model="userLastName" placeholder="">
          </label>
        </div>
        <div>
          <label>
            <span>Телефон</span>
            <input type="tel" v-model="userPhone" placeholder="">
          </label>
        </div>
        <div>
          <label>
            <span>Email</span>
            <input type="email" v-model="userEmail" placeholder="">
          </label>
        </div>
        <div>
          <label>
            <span>Дата рождения</span>
            <input type="date" v-model="userBirthday" placeholder="">
          </label>
        </div>
        <div>
          <label>
            <span>Водительский стаж</span>
            <select v-model="userDrivingExperience">
              <option value="1980">1980</option>
              <option value="2000">2000</option>
              <option value="2014">2014</option>
            </select>
          </label>
        </div>
        <div>
          <label>
            <span>Гражданство</span>
            <select v-model="userNationality">
              <option value="Россия">Россия</option>
              <option value="Украина">Украина</option>
              <option value="Белорусия">Белорусия</option>
            </select>
          </label>
        </div>
        <div>
          <label>
            <span>Регион прописки</span>
            <select v-model="userRegion">
              <option value="Краснодар">Краснодар</option>
              <option value="Ростов">Ростов</option>
              <option value="Москва">Москва</option>
            </select>
          </label>
        </div>
        <div>
          <label>
            <span>Немного о себе</span>
            <textarea name="" id="" cols="30" rows="10" v-model="userHistory"></textarea>
          </label>
        </div>
      </div>
      <div class="user-panel__result">
        <p>Имя: {{userName}}</p>
        <p>Фамилия: {{userLastName}}</p>
        <p>Телефон: {{userPhone}}</p>
        <p>Email: {{userEmail}}</p>
        <p>Дата рождения: {{userBirthday}}</p>
        <p>Водительский стаж: {{userDrivingExperience}}</p>
        <p>Гражданство: {{userNationality}}</p>
        <p>Регион прописки: {{userRegion}}</p>
        <p>Немного о себе: {{userHistory}}</p>
      </div>
    </div>
    <!-- <v-app>
      <app-header></app-header>
      <v-content>
        <router-view/>
      </v-content>
      <app-footer></app-footer>
    </v-app> -->
    <app-footer></app-footer>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader'
import AppFooter from './components/AppFooter'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppFooter
  },
  data () {
    return {
      userName: null,
      userLastName: null,
      userPhone: null,
      userEmail: null,
      userBirthday: null,
      userDrivingExperience: null,
      userNationality: null,
      userRegion: null,
      userHistory: null,
      allFields: []
    }
  }
}
</script>

<style lang="stylus" scoped>
  input, select {
    border: 1px solid;
  }
  .user-panel {
    display flex
    justify-content space-between

    &__field {

    }
    &__result {
      background-color #ccc
    }
  }
</style>

