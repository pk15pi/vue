<template>
  <div v-if="show"> it will be visible</div>
  <div>
    <div v-if="num===0"> number is zero</div>
    <div v-else> number is not zero </div>
  </div>

  <div>
    ---------------------------------------------
    <div v-if="num===0"> number is zero</div>
    <div v-else-if="num < 0"> number is negative int</div>
    <div v-else-if="num > 0"> number is positive int </div>
    <div v-else> number is non-int </div>
  </div>
  <div>
    <h3 v-show="true"> using v show</h3>
    <p> the difference between v-if and v-show: v-if
       will not be loaded in dom if it is false</p>
  </div>
 
</template>




<script>
export default {
  name: 'HelloWorld',
  data(){
    return {
      show : true,
      applyclass : true,
      num : '',
    }
  
  }
}
</script>




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
