<template>
  <br>
  <!-- printing the variable -->
  {{name}} 
  <br>

  <!-- we can also pass the variable with v-text as plain text-->
  <div v-text="name"></div> <br>

  <!-- we can pass the variable  with some html tags-->
  <div v-html="message"></div> <br>
  <div> {{message}}</div> <br>
  <div v-html="hack"></div>

  <!-- v-bind is the way to condtionally apply any class or id, 
  here if headinId is True the heaingId will be replaced with it corresponding value -->
  <h4 v-bind:id="headingId">This is id binding, see console</h4>

  <!-- apply the said proprty as per the value stored in the given variaables. way to dynamically apply the property -->
  <div>
    <button v-bind:disabled="isDisabled"> bind </button>
    <button v-bind:disabled="isActive"> bind </button>
  </div>

  <!-- bind the class with the value stored in status variable, simply use class to assign static class/property -->
  <h4 v-bind:class="status">
     status 
  </h4>

  <!-- both the class will be aplied see console-->
  <h4 v-bind:class="status" class="underline">
     status 
  </h4>

  <!-- if ispromoted is true apply promoted class, apply underline class always -->
  <h4 v-bind:class="ispromoted && 'promoted'" class="underline">
     promoted movie 
  </h4>

  <!-- usign turnery operator  -->
  <!-- if issoledout is true apply sold-out class else apply newmovie class -->
  <h4 v-bind:class="issoledout ? 'sold-out' : 'newmovie'">
     Sold out? movie 
  </h4>

  <!-- we can also directy write the css directly using v-bind:style -->
  <!-- double worded keys and any string in value to be written in quotes -->
  <!-- we pass javasccript object where the key will be css property and the value will the data property we have declared -->
  <h4 v-bind:style="{
      color : mycolor, 
      'font-style': mysize + 'px',
      padding : 5 + 'px',
  }"> we can also directly write styling in the tag itself</h4>

  <!-- we can style bind by passing javascript object to make template look clearer -->
  <h4 v-bind:style="cssJSObjet"> we can also directly write styling in the tag itself</h4>
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
       status : 'danger',
       ispromoted : false,
       mycolor : 'red',
       mysize : 5,

       cssJSObjet : {
          color : 'red', 
          'font-style': 5 + 'px',
          padding : 5 + 'px',
       }
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

.underline{
  text-decoration: underline;
}
.danger{
  text-decoration: red;
}

.promoted{
font-style: italic;
}

.newmovie{
  text-decoration: line-through;
  font-style: oblique;
}
.sold-out{
  text-decoration: underline;
  font-style: italic;
}
</style>
