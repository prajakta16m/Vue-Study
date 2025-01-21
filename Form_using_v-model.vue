/* Run using https://playcode.io/vue
*  Using v-model and reactive ref to validate form
*/
<script setup>
import {ref, computed, reactive } from 'vue'

const emailId = ref("");
const count = ref(0)
const isFormValid = () => {
  return emailId.value.length > 0;
};
</script>

<template>
  <h1>Hello Vue 3 - Form example</h1>
  <div><p>Enter email</p><input v-model="emailId" placeholder="Email Id" /></div>
  <br/>
  <button >Submit</button>
  <p>Form is {{isFormValid() ? '' : 'not'}} valid</p>
</template>

<style scoped>
button {
  font-weight: bold;
}
</style>
