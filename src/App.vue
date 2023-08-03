<script setup>
import { h, ref } from 'vue'
import { countries } from './data/countries.js'

const search = ref('') 

function getFilteredCountries() {
  return countries.filter(country => {
    return country.name.toLowerCase().startsWith(search.value.toLowerCase())
  })
}
</script>

<template>
  <section class="mx-auto container text-left">
    <div class="flex justify-center items-center">
      
      <p class="my-5">
        search:<input class="p-3 mx-3" type="text" v-model="search">
      </p>
      <p class="my-5">{{ search }}</p>
    </div>
    <div class="mt-10 grid lg:grid-cols-4 md:grid-cols-3 sm:grid-cols-2">
      <div class="bg-slate-100 m-2 p-3 rounded-lg" v-for="country in getFilteredCountries()" :key="country.code">
        {{ country.name }}
      </div>
    </div>

  </section>
</template>
<style scoped></style>