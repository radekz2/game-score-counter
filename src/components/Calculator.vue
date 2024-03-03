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
function reset() {
  score.value = 0
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
      <button @click="reset()">Reset</button>
    </div>
  </div>
</template>

<style scoped>
</style>
