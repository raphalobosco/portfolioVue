
<script setup>

const props = defineProps({ proj: Object })

</script>

<template>
  <div v-for="(item, index) in proj" :key="index">
    <p>{{ item.title }}</p>
    <img :src="item.photo" alt="">
  </div>
</template>

<style lang="scss" scoped></style>