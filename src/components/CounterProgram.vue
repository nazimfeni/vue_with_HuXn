<template>
      <div>
        <h2>Counter Component</h2>
        <button @click="increment">Count is: {{ count }}</button>
      </div>
    </template>
    
    <script setup>
    import {
      ref,
      onBeforeMount,
      onMounted,
      onBeforeUpdate,
      onUpdated,
      onBeforeUnmount,
      onUnmounted,
      onActivated,
      onDeactivated,
      onErrorCaptured
    } from 'vue';
    
    const count = ref(100);
    
    function increment() {
      count.value++;
    }
    
    // Lifecycle Hooks of Vue
    onBeforeMount(() => {
      alert('Before Mount: Component is about to be added to the DOM');
    });

    onMounted(() => {
      alert(`Mounted: The initial count is ${count.value}`);
    });
    onBeforeUpdate(() => {
      alert('Before Update: DOM is about to change');
    });
    
    onUpdated(() => {
      alert('Updated: DOM changed because of reactive update');
    });
    
    onBeforeUnmount(() => {
      alert('Before Unmount: Component will be removed from DOM');
    });
    
    onUnmounted(() => {
      alert('Unmounted: Component removed from DOM');
    });
    
    onActivated(() => {
      alert('Activated: Component is now active (keep-alive)');
    });
    
    onDeactivated(() => {
      alert('Deactivated: Component is now inactive (keep-alive)');
    });
    
    onErrorCaptured((err, instance, info) => {
      alert('Error captured in component: ' + err.message);
      return false; // prevent further propagation
    });
    </script>
    
    <style>
    h1 {
      color: teal;
    }
    </style>
    