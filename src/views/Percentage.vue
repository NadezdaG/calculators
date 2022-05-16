<template>
  <div>
    <h1>Percentage Calculator</h1>
    <p></p>

    <form>
      <input v-model="percent" /> % of <input v-model="number" /> is
      <span v-html="answer"></span>
    </form>
  </div>
</template>

<script setup>
import { computed, ref } from "vue";
let percent = ref(10);
let number = ref(100);
let answer = computed(() => {
  return (percent.value * number.value) / 100;
});
</script>
