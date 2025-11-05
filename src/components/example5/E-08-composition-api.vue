<template>
  <div>
    <h2>{{ title }}</h2>
    <p>Full Name: {{ fullName }}</p>
    <input v-model="firstName" placeholder="First Name" />
    <input v-model="lastName" placeholder="Last Name" />
    <button @click="greet">Greet</button>
    <p>Greeting Count: {{ greetCount }}</p>
    <p>{{ message }}</p>
  </div>
</template>

<script setup lang="ts">
import {
  ref, computed, watch,
  onBeforeMount, onMounted,
  onBeforeUpdate, onUpdated,
  onBeforeUnmount, onUnmounted
} from 'vue'

const props = withDefaults(defineProps<{
  title?: string
}>(), {
  title: 'User Information'
})
// eslint-disable-next-line vue/no-setup-props-destructure
const { title } = props

const firstName = ref<string>('John')
const lastName  = ref<string>('Doe')
const greetCount = ref<number>(0)
const message = ref<string>('')

const fullName = computed<string>(() => `${firstName.value} ${lastName.value}`)

const greet: () => void = () => {
  greetCount.value++
  message.value = `Hello, ${fullName.value}!`
}
const resetGreetCount: () => void = () => {
  greetCount.value = 0
}

watch(greetCount, (newValue: number, oldValue: number) => {
  console.log(`Greet count changed from ${oldValue} to ${newValue}`)
  if (newValue >= 3) {
    message.value = "That's enough greetings for now!"
  }
})

onBeforeMount(() => console.log('beforeMount hook'))
onMounted(() => console.log('mounted hook'))
onBeforeUpdate(() => console.log('beforeUpdate hook'))
onUpdated(() => console.log('updated hook'))
onBeforeUnmount(() => console.log('beforeUnmount hook'))
onUnmounted(() => console.log('unmounted hook'))
</script>
