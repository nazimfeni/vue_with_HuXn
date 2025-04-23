<script setup>
import { ref } from 'vue';
import CounterProgram from './components/CounterProgram.vue';

const show = ref(true);

function toggle (){
  show.value = !show.value;
}
</script>


<template>
  <div>
    <h1>Vue Lifecycle Demo</h1>
    <button @click="toggle">Toggle Component</button>

    <CounterProgram v-if="show" />
    <!-- <keep-alive>
      <CounterProgram v-if="show" />
    </keep-alive> -->
  
  
  </div>
</template>


