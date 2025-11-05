<template>
  <E05ParentComponent />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import E05ParentComponent from "@/components/example3/ParentComponent.vue";

export default defineComponent({
  name: 'App',
  components: {
    E05ParentComponent,
  }
});
</script>

<style>
</style>
