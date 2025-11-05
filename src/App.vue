<template>
  <e03-binding />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import E02Reactive from "@/components/example1/E-02-reactive.vue";
import E01Instance from "@/components/example1/E-01-instance.vue";
import E03Binding from "@/components/example1/E-03-binding.vue";

export default defineComponent({
  name: 'App',
  components: {
    E03Binding,
  }
});
</script>

<style>
</style>
