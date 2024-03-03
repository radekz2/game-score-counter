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
  <div class="calculator">
    <div class="main-label">{{ label }} - Score: {{ score }}</div>
    <div>
      <input class="player-name" name="playerName" placeholder="Player Name" value=""/> 
    </div>
    <div class="action-buttons">
      <button @click="substract(1)">-1</button>
      <button @click="add(1)">+ 1</button>
      <button @click="substract(5)">- 5</button>
      <button @click="add(5)">+ 5</button>
      <button @click="reset()" class="error">Reset</button>
    </div>
  </div>
</template>

<style scoped>
.action-buttons{
  display: flex;
  justify-content: space-between;
  margin-top: 0.5rem;
}
button {
  margin: 0.1rem;
}
.calculator {
  border: 0px solid #00000017;
  border-radius: 10px;
  padding: 0.3rem;
  margin: 0.5rem;
  display: inline-block;
  width: 95%;
}
.main-label {
  font-size: 1.5rem;
  font-weight: bold;
  margin-bottom: 0.5rem;
  padding: 0rem 0.5rem; 
}
.player-name {
  border: 1px solid #00000017;
  border-radius: 5px;
  margin-top: 0.3rem;
  margin-bottom: 0.6rem;
}
</style>
