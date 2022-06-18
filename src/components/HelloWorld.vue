<template>
<br>
  {{name}} <br>
  <div v-text="name"></div> <br>
  <div v-html="message"></div> <br>
  <div> {{message}}</div> <br>
  <div v-html="hack"></div>
  <h2 v-bind:id="headingId">This is id binding, see console</h2>
  <div>
    <button v-bind:disabled="isDisabled"> bind </button>
    <button v-bind:disabled="isActive"> bind </button>
  </div>
<br>
  {{msg}}
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      name : 'Prasenjit',
       message : '<b>You Are Welcome in learning vue</b>',
       hack : '<a href="#" onclick=alert("click me to see alert")> click me </a>',
       headingId: 'this is heading',
       isDisabled : true,
       isActive : false,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
