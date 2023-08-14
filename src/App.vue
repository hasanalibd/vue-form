<script setup>
  import {ref} from 'vue'
  const color = ref('None')

  function getStyle(){
    return{
      backgroundColor: color.value
    }
  }

</script>

<template>
  <section class="container mx-auto">
    <h1 class="text-2xl font-semibold my-5">Vue Form</h1>
    <p class="pb-5">Your Favorite Color: {{ color }}</p>

    <p>
      You Favorite Color: 
      <input type="text" class=""  v-model="color">
      <div :style="getStyle()" class="w-16 h-16 mt-5" ></div>
    </p>
  </section>
</template>