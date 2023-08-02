<script setup>
import { ref, reactive } from 'vue'
const displayImage = ref(true)
</script>

<!-- <template>
  <section class="mx-auto container">
    <h1 class="text-2xl mb-10">Vue Form</h1>
    <p class="mb-10">{{ displayImage }}</p>
    <label for="">Display Random Image</label>
    <input class="ml-2" type="checkbox" v-model="displayImage" />
    <p class="mt-5">
      <input type="radio" name="display" :value="true" v-model="displayImage"> On <br/>
      <input type="radio" name="display" :value="false" v-model="displayImage"> Off <br/>
    </p>
    <img
      v-show="displayImage"
      class="mt-10 mx-auto w-[500px]"
      :src="`https://source.unsplash.com/random`"
      alt=""  />
      
      <img
      v-if="displayImage"
      class="mt-10 mx-auto w-[500px]"
      :src="`https://source.unsplash.com/random?version=${Math.random()}`"
      alt=""  />

  </section>
</template> -->

<template>
  <section class="mx-auto container">
    <h1 class="text-2xl mb-10">Vue Form</h1>
    <p>{{ displayImage }}</p>
    <label for="">Display Random Image</label>
    <!-- <input type="checkbox" name="" id="" class="ml-2" v-model="displayImage"> -->
    <p class="mt-5">
      <input type="radio" name="display" id="" :value="true" v-model="displayImage"> On <br>
      <input type="radio" name="display" id="" :value="false" v-model="displayImage"> Off <br>
    </p>
    <!-- <img
      v-show="displayImage" 
      :src="`https://source.unsplash.com/random`"
      class="mt-5 mx-auto w-[600px]"
      alt=""> -->
      <img
        v-if="displayImage"
        class="mt-10 mx-auto w-[500px]"
        :src="`https://source.unsplash.com/random?version=${Math.random()}`"
        alt=""  />
  </section>
</template>
