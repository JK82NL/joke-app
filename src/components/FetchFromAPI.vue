<script setup lang="ts">
import { ref, computed } from 'vue'
import { useFetch } from '../useFetch.ts'

// Use These hooks
// beforeFetch
// afterFetch

const baseUrl = 'https://v2.jokeapi.dev/joke/any/'
const id = ref('1')
const url = computed(() => baseUrl + id.value)

const { data, error } = useFetch(url)

const retry = () => {
  id.value = ''
  id.value = '1'
}
</script>

<template>
  Load post id:
  <button v-for="i in 5" @click="id = `${i}`">{{ i }}</button>
  <div v-if="error">
    <p>Error Encountered: {{ error }}</p>
    <button @click="retry">Retry</button>
  </div>
  <div v-else-if="data">
    Data Loaded:
    <pre>{{ data }}</pre>
  </div>
  <div v-else>Loading...</div>
</template>

<style scoped></style>
