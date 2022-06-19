<template>
 <div>
  <h5>{{name}}</h5>
  <!-- <button v-on:click="name = 'preesha'"> onclick </button> &nbsp;&nbsp;
  <button v-on:mouseover="name = 'preesha'"> on mouse hover </button> -->
  <button @click="name = 'sudha'"> onclick </button> &nbsp;&nbsp;
  <button @mouseover="name = 'preesha'"> on mouse hover </button> &nbsp;&nbsp;
  <button @mouseover="name = 'prasenjit'"> reset on hover </button>
  <br>
  <h4> {{count}}</h4>
  <!-- <button v-on:click="count += 1"> increment </button>
  <button v-on:click="count -= 1"> decrement </button> -->
  <button @click="incr($event)"> increment </button>
  <button @click="decr"> decrement </button>
  <br>
  <button @click="changeName"> console the event </button>
  <button @click="changeName($event), incr($event)"> execute multiple methods </button>
 </div>

 <div>
  
 </div>
</template>




<script>
export default {
  name: 'HelloWorld',
  data(){ 
    return {
   name : 'prasenjit',
   count : 0
  }
  },
  methods : {
    changeName(event) {
      console.log('Event', event)
      this.name = 'name is changed'
    },
    incr(event){
      console.log('Event', event)
      return this.count += 1
    },
    decr(){
      return this.count -= 1
    }
  }
}
</script>




<style scoped>

</style>
