<template>
  <div id="app">
      <h1>{{ msg }}</h1>
      <h2 style="color:red;">{{decs}}</h2>
        <h3>Essential Links</h3>

    <ul>
      <li><a target="_blank" href="https://github.com/Rise-Devin/vue-devin">GitHub</a></li>
      <li v-for="item in menu"><router-link :to="item.name">{{item.name}}</router-link></li>
      
    </ul>
    <h4>{{suggestion}}</h4>
    <router-view></router-view>
  </div>
</template>

<script>

export default {
  name: 'app',
  data () {
    return {
      menu:require('./menu.js'),
      msg: 'Welcome to Use vue-devin',
      decs:'Please starred me if you like it. Many thanks!',
      suggestion:'If you have some ideas,Welcome to present!'
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
