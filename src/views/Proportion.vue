<template>
  <div>
    <h1>Proportion Calculator</h1>
    <p>
      The Proportion Calculator is used to solve proportion problems and find
      the missing value in a proportion.
    </p>

    <form>
      <input v-model="fraction1a" /> = <input v-model="fraction1b" />
      <br /><input v-model="fraction2a" /> =
      <input v-model="fraction2b" disabled />
    </form>
  </div>
</template>

<script setup>
import { computed, ref } from "vue";
let fraction1a = ref(0);
let fraction1b = ref(0);
let fraction2a = ref(0);
let fraction2b = computed(() => {
  return (fraction2a.value * fraction1b.value) / fraction1a.value;
});
</script>
