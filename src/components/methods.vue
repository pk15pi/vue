<template>
 <div>
  <h5>add from html  {{ 5 + 3 + 5}}</h5>
  <h5>add by script methods  {{ add(5,3,5) }}</h5>
  <h5>Multifply by methods {{ multiply(10)}}</h5>
  <h5>Multifply by methods {{ multiply(basevalue2)}}</h5>
 </div>

 <div>
    using template to show full name :  {{firstname}} {{lastname}}
    using computed properties : {{ fullname }}
 </div>

 <div>
  <button @click="items.push({id:3, title:'mouse', price:50})">add item </button>
 </div>
  <h2>
    <!-- using compute is helpful in case of reusing the computed value, we need not to compute at every called place -->
  Total - {{items.reduce((total,curr)=>(total = total+curr.price),0)}}
  using compute - {{total}}
  </h2>

</template>




<script>
export default {
  name: 'HelloWorld',
  data(){
    return {
      show : true,
      baseMuliplier : 5,
      basevalue2 : 8,

      firstname : "prasenjit",
      lastname : "kushwaha",
      items:[
        {
            id:1,
            title:'TV',
            price:100,
        },
        {
            id:2,
            title:'Radio',
            price:500,
        },
    ]

    }
  },
  methods: {
    add(a, b, c) {
      return (a + b + c)
    },
    multiply(num) {
      return (num * this.baseMuliplier)
    },
  },

  // this is the concept of computed properties
  // the difference between methods and compute is that the computes are cached while method gets executed every time.
  computed: {
    // fullname() {
    //   return '${this.firstname} ${this.lastname}'
    // },

    // we need to use getter and setter to use it effectively 
     fullname : {
      get(){
      return '${this.firstName} ${this.lastName}'
      },
        set(value){
          const names=value.split('')
          this.firstName=names[0]
          this.lastName=names[1]
      },
   
    total() {
      return this.items.reduce((total,curr)=>(total = total+curr.price),0)
    }

  }
}
}
</script>




<style scoped>

</style>
