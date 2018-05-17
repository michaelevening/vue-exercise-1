<template>
  <div id="app">




    <input type="email" v-model="email"><button @click="alertMyEmail()">Wyświetl mój e-mail w alercie</button>
    <h1>Twój email to: {{ email }}</h1>

<div v-if="email.length < 10">Ale masz krótki adres!</div>
<div v-else-if="email.length < 15">Twój adres e-mail jest w sam raz.</div>
<div v-else>Twój adres e-mail jest stanowczo za długi.</div>


<h1>Witaj w systemie zapisów na zajęcia</h1>
Zaloguj się emailem <input type="login" v-model="login"><button @click="login()">Wchodzę</button>

<h2>Witaj {{ login }}</h2>

 
  </div>

</template>

<script>

export default {
              methods: {
              alertMyEmail() {
              alert(this.email) },
              login(){
                return {login:''}
              }
},

    name: 'app',
  data () {
    return {
      msg: 'Hello W',
      email: '',
      password: ''
          }
    }       
    } 


</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
