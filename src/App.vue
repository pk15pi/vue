<template>
  <div>every app is registered in App.vue</div>
  <div>
    <table>
      <tr>
        <td> <HelloWorld msg="Welcome to Your Vue.js App"/></td>
        <td> <ifelse /> </td>
        <td><list/></td>
      </tr>
    </table>

  </div>
  
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ifelse from './components/ifelse.vue'
import List from './components/list.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    ifelse,
    List
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}



.thalign {
  align-self: auto;
}
</style>
