<template>
  <div>
     Parent component
     <button @click="showChild=!showChild">Toggle child</button>
    <MyChild v-if="showChild" />
  </div>
</template>

<script>
    import MyChild from './Child.vue'
    export default{
    name:'ParentComponent',

    components : {
        MyChild,
    },

    data(){
        return {
            showChild:true,
        }
        },
        beforeCreate(){
        console.log('parent beforeCreate()')
        },
        created(){
        console.log('parent created()')
        },
        beforeMount(){
        console.log('parent beforeMount()')
        },
        mounted(){
        console.log('parent mounted()')
        },
        beforeUpdate(){
        console.log('parent beforeUpdate()')
        },
        updated(){
        console.log('parent updated()')
        }
    } 
</script>


<style>
</style>
     
        
