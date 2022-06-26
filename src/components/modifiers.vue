<template>
<div>
  <pre>
    {{ JSON.stringify(formValues, null, 2)}}
  </pre>
</div>
  <form @submit="SubmitForm">
    <div>
      <label for="name"> Name </label>
      <!-- trim removes any spaces before or after -->
      <input type="text" id="name" v-model.trim="formValues.name" />
    </div>

    <div>
      <label for="age"> Age </label>
      <!-- number ensures the data is number (55) not string ("55")  -->
      <input type="number" id="age" v-model.number="formValues.age" />
    </div>

    <div>
      <label for="profile_summary">Summary </label>
      <textarea type="text" id="profile_summary" v-model="formValues.profile_summary" />
    </div>

    <div>
      <label for="country"> Country </label>
      <select id="country" v-model="formValues.country">
        <option value=""> Select a Country </option>
        <option value="india"> India </option>
        <option value="australia"> Australia </option>
        <option value="singapore"> Singapore </option>
      </select>
    </div>
    
    <div>
      <label for="joblocation"> Job Location </label>
      <select id="joblocation" v-model="formValues.joblocation">
        <option value=""> Select a Country </option>
        <option value="india"> India </option>
        <option value="australia"> Australia </option>
        <option value="singapore"> Singapore </option>
      </select>
    </div>

    <div>
      <label for="remoteWork"> Open to work remotely</label>
      <input type="checkbox" id="remoteWork" 
      v-model="formValues.remoteWork"
      true-value="yes" false-value="no"
      />
    </div>

    <div>
      <label> Skill Set </label>
      <input type="checkbox" id="html" value="html" v-model="formValues.skills" />   
      <label for="html"> Open to work remotely</label>

      <input type="checkbox" id="php" value="php" v-model="formValues.skills" />
      <label for="php"> Open to work remotely</label>

      <input type="checkbox" id="python" value="python" v-model="formValues.skills" />
      <label for="python"> Python </label>     
    </div>
    
    <div>
      <label>Years of Experience</label>
      <input
        type="radio"
        id="0-2"
        value="0-2"
        v-model="formValues.experience" />
      <label for="0-2">0-2</label>

      <input
        type="radio"
        id="3-5"
        value="3-5"
        v-model="formValues.experience" />
      <label for="3-5">3-5</label>

      <input
        type="radio"
        id="6-10"
        value="6-10"
        v-model="formValues.experience" />
      <label for="6-10">6-10</label>
    </div>

    <div>
      <button> Submit</button>
    </div>
  </form>
</template>


 

<script>
export default {
  name: 'HelloWorld',
  data(){
    return {
      formValues : {
        name: '',
        profile_summary:'',
        country : '',
        joblocation : '',
        // remoteWork : false,
        remoteWork : 'no',
        skills : [],
        experience : [],
        age : null,
      },
    }
  },
  methods :{
    SubmitForm(event){
      // by default on submit the page gets refreshed, to prevent that user preventdefault
      event.preventDefault()
      console.log('form values', this.formValues)
    }
  }
}

</script>



<style scoped>

</style>
