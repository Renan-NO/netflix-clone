<template>
  <header class="main-header">
    <nav class="menu-navigation">
      <a class="logo" href=""><img src="logo.svg"></a>
      <ul class="navigation-tab">
        <li v-for="tab in tabs" :key="tab">
          <a>{{ tab.name }}</a>
        </li>
      </ul>
    </nav>
      <header-profile />
  </header>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs } from 'vue'
import HeaderProfile from './HeaderProfile.vue'

export default defineComponent({
  name: 'Header',
  components: { HeaderProfile },
  setup() {
    const data = reactive({
      tabs: [
        { name: 'Inicio' },
        { name: 'Séries' },
        { name: 'Filmes' },
        { name: 'Bombando' },
        { name: 'Minha Lista' },
        { name: 'Navegar por idiomas' }
      ]
    })
    return { ...toRefs(data) }
  }
})
</script>

<style>
.main-header {
  display: flex;
  align-items: center;
  height: 68px;
  padding: 0 60px;
  width: 100%;
  background-image: linear-gradient(to bottom,rgba(0,0,0,.7) 10%,rgba(0,0,0,0));
}

.menu-navigation {
  display: flex;
  flex-direction: row;
  width: 100%;
}
.logo {
  text-decoration: none;
  max-width: fit-content;
  max-height: fit-content;
}

.logo img {
  margin-top: 5px;
  width: 85%;
  height: 1.89rem;
  padding-right: 15px;
}

.navigation-tab {
  position: relative;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;

  padding: 0;

  list-style-type: none;
}

.navigation-tab li {
  padding: 0 10px;
  font-size: 15px;
  font-weight: 300;
  color: #E5E5E5;
}

.navigation-tab li a {
  text-decoration: none;
  white-space: nowrap;
}
</style>
