<script setup lang="ts">
import { computed, reactive } from "vue";

const data = reactive({
  a: 0,
  b: 0,
  c: 0,
});

//const answer = computed(() => data.a + data.b);

const solve = () => (data.c = data.a + data.b);
</script>

<template>
  <div>
    <div><input type="text" v-model="data.a" /></div>
    <div><input type="text" v-model="data.b" /></div>
    <button @click="solve">Solve</button>
    <p>Result</p>
    <div>{{ data.c }}</div>
  </div>
</template>
