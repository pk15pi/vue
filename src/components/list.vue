<template>
  <div>
    <h4 v-for="(name, i) in names" :key="name">{{ i }} {{ name }}</h4>
  </div>

  <div>
    <h4 v-for="(name, index) in fullnames" :key="name">{{ index }} {{ name.first }} {{ name.last }}</h4>
  </div>
 
  <div v-for="actor in actors" :key="actor">
    <h4 > {{ actor.name }} </h4>
    <h4 v-for="movie in actor.movies" :key="movie"> {{ movie }} </h4>
  </div>
 
</template>




<script>
export default {
  name: 'HelloWorld',
  data(){
    return {
      names: ['prasenjit', 'preesha', 'sudha'],
      fullnames : [
        {first: 'prasenjit',  last : 'kushwaha'},
        {first: 'sudha',  last : 'kushwaha'},
      ],
      actors : [
        {
          name: 'prasenjit',  
          movies : ['movie1','movie2'],
        },
        {
          name: 'preesha',  
          movies : ['movie5','movie6'],
        }
      ]
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
