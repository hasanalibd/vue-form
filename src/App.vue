<script setup>
import { ref, reactive } from 'vue'
const favColors = ref([])

</script>

<template>
  <section class="mx-auto container">
    <h1 class="text-2xl mb-10">Vue Form</h1>
    <p class="mb-10">{{ favColors }}</p>
    Your favorite colors <br/>
    <label for="red">Red</label>
    <input type="checkbox" class="mx-2" value="red" v-model="favColors">
    <label for="blue">Blue</label>
    <input type="checkbox" class="mx-2" value="blue" v-model="favColors">
    <label for="green">Green</label>
    <input type="checkbox" class="mx-2" value="green" v-model="favColors">
  </section>
</template>
<style scoped></style>