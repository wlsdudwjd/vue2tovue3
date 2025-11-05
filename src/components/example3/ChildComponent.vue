<template>
  <div>
    <p>{{ message }}</p>
    <button @click="emit('custom-event', 'Hello from child')">Send Event</button>
  </div>
</template>

<script setup>
const emit = defineEmits(['custom-event'])

defineProps({
  message: {
    type: String,
    required: true
  }
})
</script>