
import { ref } from 'vue'
<script>  
export default {
  name: 'HelloWorld',
  props: {
    msg: String,
  },
  setup(props) {
    const count = ref(0)
    return {
      count,
    }
  },
}


defineProps({
  msg: String,
})
</script>
<template>

<button type="button" @click="count++">
  count is: {{ count }} <br></button>


  
</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>