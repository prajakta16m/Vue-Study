/*
 * Play in https://playcode.io/vue
 * Enter value in input, press key event and see count updated. Understanding key events handling with inline arguments
*/
<script setup>
import {ref} from 'vue'

const count = ref(0)
</script>

<template>
  <h1>Hello Vue 3</h1>
  <button @click.stop="count++">Count is : {{ count }}</button>
  <input @keyup.enter =" ($event) => {count = $event.target.value} "  placeholder="Enter here" />
</template>

<style scoped>
button {
  font-weight: bold;
}
</style>
