<template>
<div>
  <pre>
    {{ JSON.stringify(formValues, null, 2)}}
  </pre>
</div>
  <form>
    <label for="name"> Name </label>
    <input type="text" id="name" v-model="formValues.name" />
    <label for="name"> Profile Summary </label>
    <input type="text" id="profile_summary" v-model="formValues.profile_summary" />
  </form>
</template>


<script>
export default {
  name: 'HelloWorld',
  data(){
    return {
      formValues : {
        name: '',
        profile_summary:''
      },
    }
  }
}

</script>



<style scoped>

</style>
