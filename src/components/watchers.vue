<!-- watchers are the mechanism to monitor any changes in any variables / volume  -->

<!-- this is the program that will alert the user at 16 when it keeps on increasing the value -->
<!--  -->

<template>

<h2> Volume Tracker(0-20) </h2>
<h3> Current Volume-{{volume}}</h3>
<div>
  <button @click="volume-=2">Decrease</button>
  <button @click="volume+=2">Increase</button>
</div>

</template>




<script>
export default {
  name: 'HelloWorld',

data(){
  return{
    volume:0,
 }
},
methods:{},
computed:{},

watch:{
  // oldValue is added to give a condition to alert only while increasing the value not while decreasing
  volume(newValue , oldValue){
    if(newValue > oldValue && newValue === 16 ) {
      alert(
        'Listening to high volume may damage your hearings'
     )
    }
    },
},
}
</script>


}
</script>




<style scoped>

</style>
