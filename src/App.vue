<script setup lang="ts">
// import { RouterLink, RouterView } from 'vue-router'
import FetchFromAPI from './components/FetchFromAPI.vue'
import StyleTesting from './components/StyleTesting.vue'
</script>

<template>
  <!-- <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header> -->
  <h1>Heading 1</h1>
  <h2>Heading 2</h2>
  <p>Main Text</p>
  <span>Subtext</span>

  <div>
    <FetchFromAPI />
  </div>
  <div>
    <StyleTesting />
  </div>

  <!-- <RouterView /> -->
</template>

<style scoped></style>
