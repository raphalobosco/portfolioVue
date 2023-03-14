<script>
import sourceData from "../data/data.json";
import { ref, computed } from "vue";

export default {
  computed: {
    projectId() {
      return this.$route.params.id;
    },
    project() {
      return sourceData.projects.find(
        (project) => project.id === this.projectId
      );
    },
  },
};

// const projectId = computed(() => {
//     return
// })

// const project = computed(() => {
//     return sourceData.projects.find(project => project.id === projectId.value)
// })
</script>

<template>
  <div>
    <div>
      <h1>{{ project.title }}</h1>
      <p>{{ project.desc }}</p>
      <img :src="project.photo" alt="" />
    </div>
  </div>
</template>
<style lang="scss" scoped></style>
