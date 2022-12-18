
<script setup>  
import { ref } from 'vue'

<h1>I don't even know whats happening yet! 🤣</h1>


defineProps({
  msg: String,
})

const count = ref(0)
</script>

<template>
  <h1>{{ msg }}</h1>
  
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
</script>