<script setup>

import { ref } from 'vue';
import sourceData from '../data/data.json'
import ProjectsGrid from '../components/ProjectsGrid.vue';

const props = ref(sourceData.projects)

const projects = sourceData.projects

</script>

<template>
    <div>

        <router-link v-for="project in projects " :key="project.id" :to="'/project/' + project.id">
            <p> {{ project.title }}</p>
            <img :src="project.photo" alt="">
        </router-link>

        <!-- <ProjectsGrid :proj="props" /> -->


    </div>
</template>

<style lang="scss" scoped></style>