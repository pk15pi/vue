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
        <!-- <td> <Methods/></td> -->
        <!-- <td> <EventListeners/></td> -->
        <!-- <td> <Forms/></td> -->
      </tr>
      <tr>
        <!-- <td> <Modifiers/></td> -->
        <!-- <td> <dynamicComp/></td> -->
        <!-- <td> <Parent/> </td> -->
      </tr>
      <tr>
        <!-- <td> <PostList/></td> -->
        <!-- <td> <TempRef/></td> -->
        <!-- <td> <MyComp1/></td> -->
      </tr>
      <tr>
        <!-- <td> <MyComp2/></td> -->
        <td> <MainAppVuetify /></td>
      </tr>
    </table>

  </div>
  
</template>

<script>
import 'vuetify/dist/vuetify.min.css'

// import HelloWorld from './components/HelloWorld.vue'
// import ifelse from './components/ifelse.vue'
// import List from './components/list.vue'
// import Methods from './components/methods.vue'
// import EventListeners from './components/eventListeners.vue'
// import Forms from './components/forms.vue'
// import Modifiers from './components/modifiers.vue'
// import Modifiers from './components/modifiers.vue'
// import dynamicComp from './components/dynamicComponents.vue'
// import Parent from './components/LifeCHooks/Parent.vue'
// import PostList from './components/LifeCHooks/CallOnPageLoad.vue'
// import TempRef from './components/LifeCHooks/templateRefs.vue'
// import MyComp1 from './components/mixins/comp1.vue'
// import MyComp2 from './components/mixins/comp2.vue'
import MainAppVuetify from '../src/components/workwithvuetify/mainpage.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    // ifelse,
    // List,
    // Methods,
    // EventListeners,
    // Forms,
    // Modifiers,
    // dynamicComp, **have some isssue
    // Parent,
    // PostList,
    // TempRef,
    // MyComp1,
    // MyComp2,
    MainAppVuetify,
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
