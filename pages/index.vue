<script setup>
// Fetch All Post
const { data, error, pending } = useLazyFetch(
  "https://dummyjson.com/posts?limit=10"
);
// console.log(data);

// const { data: products } = useFetch("/api/products");
// console.log(products);
useHead({
  title: "Home",
});
</script>

<template>
  <div>
    <div v-if="error" class="text-2xl text-white">
      An error occured... {{ error }}
    </div>
    <div v-else-if="data">
      <div v-for="{ id, title, body } in data.posts" :key="id">
        <PostCard :id="id" :title="title" :body="body" />
      </div>
    </div>
    <div v-else class="text-2xl text-white">Loading...</div>
  </div>
</template>

<style lang="css" scoped></style>
