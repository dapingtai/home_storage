<script setup lang="ts">
import { reactive } from "vue";
import { RouterLink } from 'vue-router'
const barData = reactive(['Home', 'Login'])

</script>

<template>
  <nav class="w-screen px-2 sm:px-4 py-2.5 bg-white border-gray-200 rounded dark:bg-gray-800">
    <div class="hidden justify-between items-center w-full md:flex md:w-auto md:order-1">
      <ul class="flex flex-col mt-4 md:flex-row md:space-x-8 md:mt-0 md:text-sm md:font-medium">
        <li v-for="(item, index) in barData" :key="index" class="cursor-pointer">
          <RouterLink :to="`/${item.toLowerCase()}`">
            <span class="block py-2 pr-4 pl-3 bg-blue-700 rounded md:bg-transparent text-white
              md:text-white md:p-0 dark:text-white" >
              {{ item }}
            </span>
          </RouterLink>
        </li>
      </ul>
    </div>
  </nav>
</template>

<style>

</style>
