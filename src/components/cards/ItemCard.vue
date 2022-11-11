<script setup>
import { RouterLink } from 'vue-router';

defineProps({
  id: Number,
  title: String,
  category: String,
  image: String,
});

</script>

<template>
  <div class="w-full px-1 my-1 md:w-1/2 lg:my-4 lg:px-4 lg:w-1/3">
    <RouterLink :to="'/products/' + id">
      <div class="overflow-hidden border border-gray-200 rounded-xl hover:border-gray-300 hover:shadow-md group">

        <div class="m-4 overflow-hidden rounded-xl">
          <img :alt="title" class="block w-full h-auto" :src="'/src/assets/img/' + image" />
        </div>


        <header class="px-4 mb-4 leading-tight">
          <h1 class="text-lg">
            <RouterLink class="font-semibold text-black no-underline hover:underline" :to="'/products/' + id">
              {{ title }}
            </RouterLink>
          </h1>
          <span class="block text-sm font-light text-gray-500 no-underline">
            {{ category }}
          </span>
        </header>
      </div>
    </RouterLink>
  </div>
</template>