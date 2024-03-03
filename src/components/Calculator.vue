<script setup>
import { ref } from 'vue'
const props = defineProps(['label'])

const score = ref(0)

function add(val) {
  score.value += val
}
function substract(val) {
  score.value -= val
}
</script>

<template>
  <div>
    <h1>{{ label }} - Score: {{ score }}</h1>
    <div>
      <input name="playerName" placeholder="Player Name" value=""/> 
    </div>
    <div role="group">
      <button @click="substract(1)">-1</button>
      <button @click="add(1)">+ 1</button>
      <button @click="substract(5)">- 5</button>
      <button @click="add(5)">+ 5</button>
      <button @click="substract(10)">- 10</button>
      <button @click="add(10)">+ 10</button>
    </div>
  </div>
</template>

<style scoped>
</style>
