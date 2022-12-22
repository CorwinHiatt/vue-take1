<script setup>
import MyForm from './components/MyForm.vue'
</script>

<template>
  <div>
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  <MyForm msg="Vite + Vue" />
</template>

<style scoped>
.app{
  text-align: center;
  color: #e90acf;
  margin-top: 60px;
}
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #e40facaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #f9054aaa);
}
</style>
