<script setup>
defineProps(["id", "title", "body"]);
const image = ref("/images/banner.jpg");
</script>

<template>
  <div class="max-w-5xl mx-auto bg-gray-600 shadow-lg overflow-hidden">
    <img :src="image" alt="Post Image" class="w-full h-96 object-cover" />
    <div class="p-6">
      <h1 class="text-white text-3xl font-bold mb-4">{{ title }}</h1>
      <p class="text-gray-200 text-lg mb-4">{{ body }}</p>
      <p class="text-gray-200 text-lg mb-4">{{ body }}</p>
      <p class="text-gray-200 text-lg mb-4">{{ body }}</p>
      <p class="text-gray-200 text-lg mb-4">{{ body }}</p>

      <div class="flex items-center mt-10">
        <span class="mr-2 text-white">Share on:</span>
        <NuxtLink to="#" target="_blank" class="mr-2">
          <Icon name="uil:facebook" class="text-white" />
        </NuxtLink>
        <NuxtLink to="#" target="_blank" class="mr-2">
          <Icon name="uil:twitter" class="text-white"></Icon>
        </NuxtLink>
        <NuxtLink to="#" target="_blank" class="mr-2">
          <Icon name="uil:linkedin" class="text-white"></Icon>
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<style lang="css" scoped></style>
