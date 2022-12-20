<template>
  <div>
    <input type="text" placeholder="name" v-model="name"/> 

  </div>
  <div>
    <input type="text" placeholder="email"/>
  </div>
  <div>
    <button type="submit">Submit</button>
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
    const submit = () => {
      console.log(name.value, email.value)
    }
    return {
      name,
      email,
      submit
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
  background-color: #000;
  color: #fff;
}
</style>