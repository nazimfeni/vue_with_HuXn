<script setup>
import { reactive } from 'vue'
let initState = reactive({ count: 0 })
</script>

<template>
  <h1>Count: {{ initState.count }}</h1>
  <button @click="initState.count++">+</button>
  <button @click="initState.count--">-</button>
</template>
<style scoped></style>
