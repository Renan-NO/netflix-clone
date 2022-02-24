<template>
  <Header />
</template>

<script lang="ts">
import Header from './components/header/Header.vue'
export default {
  name: 'App',
  components: { Header }
}
</script>

<style>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
 
body, html {
  background: #141414;
  color: #fff;
  line-height: 1.2;
  user-select: none;
  font-family: 'Roboto', sans-serif;
  cursor: default;
}

#app {
  display: flex;
  align-items: center;
}
</style>
