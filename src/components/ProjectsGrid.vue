<script setup>
const props = defineProps({ proj: Object });
</script>

<template class="container">
  <div v-for="(item, index) in proj" :key="index">
    <p>{{ item.title }}</p>
    <img :src="item.photo" alt="" />
  </div>
</template>

<style>
.container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
}

img {
  width: 100%;
}
</style>
