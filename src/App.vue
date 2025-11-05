<template>
  <e12-ref-component/>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import E12RefComponent from "@/components/example6/E-12-ref-component.vue";

export default defineComponent({
  name: 'App',
  components: {
    E12RefComponent
  }
});
</script>

<style>
</style>
