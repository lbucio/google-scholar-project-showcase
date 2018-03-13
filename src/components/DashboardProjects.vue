<template>
  <div class="projects">
      <h2 class="title">Projects</h2>

      <div class="projects-container">
        <dashboard-project v-for="(project, index) in projects" :project="project" v-bind:key="index"></dashboard-project>
      </div>
  </div>
</template>

<script>
import DashboardProject from './DashboardProject';
import * as projects from '../data/projects.json';

export default {

  data() {
    return {
      projects: [],
    };
  },

  mounted() {
    this.projects = projects.data;
  },

  components: {
    DashboardProject,
  },

};
</script>

<style lang="scss">

</style>
