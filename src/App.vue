<template>
  <E01Instance />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import E01Instance from "@/components/example1/E-01-instance.vue";

export default defineComponent({
  name: 'App',
  components: {
    E01Instance
  }
});
</script>

<style>
</style>
