<!-- <script>
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

</script> -->

<script setup>
import { computed } from "vue";
import sourceData from "../data/data.json";
import { useRoute } from "vue-router";

const route = useRoute();

const projects = sourceData.projects;
const projId = route.params.id;

console.log(projId);

const project = computed(() =>
  projects.find((project) => project.id === projId)
);
console.log(project);
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
