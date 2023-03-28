<script>
export default {
  name: 'App',

  data() {
    return {
      firstName: 'Nome',
      middleName: '',
      lastName: 'Cognome',
      age: 39
    }
  },
  methods: {
    incrementAge(){
      this.age++;
    },
    // getFullName(){
    //   console.log('ho eseguito il metodo getFullName');
    //   return `${this.firstName} ${this.middleName} ${this.lastName}`
    // }
  },
  computed: {
    getFullName(){
      console.log('ho eseguito la computed getFullName');
      return `${this.firstName} ${this.middleName} ${this.lastName}`
    }
  }
}
</script>

<template>
  <h1>{{ getFullName }}</h1>
  <div>
    <label>Firstname</label>
    <input type="text" v-model="firstName">
  </div>
  <div>
    <label>middleName</label>
    <input type="text" v-model="middleName">
  </div>
  <div>
    <label>lastName</label>
    <input type="text" v-model="lastName">
  </div>
  <div>
    <label>age</label>
    <input type="number" v-model="age">
    <button @click="incrementAge">Increment</button>
  </div>
</template>


<style lang="scss">
//versione 1 - inclusione via app.vue
// @use './assets/scss/main.scss' as *;
</style>


