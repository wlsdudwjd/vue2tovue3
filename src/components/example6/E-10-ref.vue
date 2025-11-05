<template>
  <div>
    <p>Count: {{ count }}</p>
    <button @click="increment">Increment</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const count = ref(0)

function increment() {
  count.value++
}
</script>