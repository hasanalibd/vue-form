<script setup>
import { ref, reactive } from 'vue'

const person = reactive({
  name: 'John Doe',
  age: 30,
  job: 'Web Developer',
})

const user = reactive({
  name: 'Hasan Ali',
  age: 30,
  job: 'Web Developer',
  phone: '+8801850030472',
  email: 'hasanali12522@gmail.com',
})

</script>

<template>
  <section class="mx-auto container">
    <h1 class="text-2xl mb-10">Vue Form</h1>
    <p class="mb-10">
      {{ user }}
    </p>
    
    <!-- <div class="flex flex-col mb-5 text-left" v-for="(value, key, index) in person" :key="index">
      <label class="pl-3" for="name">{{ key }}</label>
      <input type="text" class="border border-gray-300 rounded-md p-2" v-model="person[key]" />
    </div> -->

    <!-- <div class="flex flex-col mb-5 text-left" v-for="(value, key, index) in person" :key="index">
      <label class="pl-3" for="name">{{ key }}</label>
      <input type="text" class="border border-gray-300 rounded-md p-2" v-model="person[key]"/>
    </div> -->

    <!-- <div class="flex flex-col mb-5 text-left" v-for="(value, key, index) in person" :key="index">
      <label for="name" class="ml-2">{{ key }}</label>
      <input type="text" class="border border-gray-300 rounded-xl p-2" v-model="person[key]">
    </div> -->

    <!-- <div class="flex flex-col mb-5 text-left" v-for="(value, key, index) in person" :key="index">
      <label for="name" class="ml-2">{{ key }}</label>
      <input type="text" class="border border-gray-300 rounded-xl p-2" v-model="person[key]">
    </div> -->

    <div class="flex flex-col mb-5 text-left" v-for="(value, key, index) in user" :key="index">
      <label for="name" class="ml-2">{{ key }}</label>
      <input type="text" class="border border-gray-300 rounded-xl p-2" v-model="user[key]">
    </div>

  </section>
</template>
<style scoped></style>