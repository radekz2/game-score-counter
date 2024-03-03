<script setup>
import { ref, onMounted } from 'vue'

const count = ref(0)
</script>

<template>
  <div>
    <h1>Player</h1>
    <div>
      <input name="playerName" placeholder="Player Name" value=""/> 
    </div>
    <div>
      Score <span id="score">{{ count }}</span>
    </div>
    <div>
      <button @click="count--">-</button>
      <button @click="count++">+</button>
    </div>
  </div>
</template>

<style scoped>
</style>
