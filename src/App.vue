<template>
  <div class="underline">every app is registered in App.vue</div>
  <div>
    <table class="table">
      <!-- <tr class="table">
        <td> <HelloWorld msg="Welcome to Your Vue.js App"/></td>
        <td> <ifelse /> </td>
        <td><list/></td>
      </tr> -->
      <tr>
        <td> <Methods/></td>
        <td> <EventListeners/></td>
        <td> <Forms/></td>
      </tr>
    </table>

  </div>
  
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
// import ifelse from './components/ifelse.vue'
// import List from './components/list.vue'
import Methods from './components/methods.vue'
import EventListeners from './components/eventListeners.vue'
import Forms from './components/forms.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    // ifelse,
    // List,
    Methods,
    EventListeners,
    Forms
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

.underline {
  text-decoration: underline;
}

.table{
  border: red, solid, 2px;
}

.thalign {
  align-self: auto;
}
</style>
