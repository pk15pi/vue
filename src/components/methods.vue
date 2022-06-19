<template>
 <div>
  <h5>add from html  {{ 5 + 3 + 5}}</h5>
  <h5>add by script methods  {{ add(5,3,5) }}</h5>
  <h5>Multifply by methods {{ multiply(10)}}</h5>
  <h5>Multifply by methods {{ multiply(basevalue2)}}</h5>
 </div>

 <div>
  
 </div>
</template>




<script>
export default {
  name: 'HelloWorld',
  data(){
    return {
      show : true,
      baseMuliplier : 5,
      basevalue2 : 8
    }
  },
  methods: {
    add(a, b, c) {
      return a + b + c
    },
    multiply(num) {
      return num * this.baseMuliplier
    }
  },
}
</script>




<style scoped>

</style>
