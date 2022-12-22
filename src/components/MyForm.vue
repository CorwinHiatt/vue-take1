<template>
  <div>
    <input type="text" placeholder="River" v-mod/> 

  </div>
  <div>
    <input type="text" placeholder="email"/>
  </div>
  <div>
    <button @:click="submitForm">Submit</button>
  </div>
  <router-view>

  </router-view>
    
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'MyForm',
  setup() {
    const name = ref('')
    const email = ref('')
    const submitForm = () => {
      console.log(`Form submitted!!! Name = ${name.value, email.value}`)
    }
    return {
      name,
      
      submitForm,
    }
  }
}
</script>

<style>
input[ type="text"]{
  padding: 20px;
  margin-bottom: 0.4ch;
}

button[type="submit"]{
  padding: 20px;
  margin-top: 0.4ch;
  background-color: rgb(242, 15, 15);
  color: rgb(244, 16, 206);
}
</style>