<template>
  <section class="dashboard">

      <dashboard-projects></dashboard-projects>

  </section>
</template>

<script>
import DashboardProjects from '../components/DashboardProjects';

export default {

  data() {
    return {
      msg: 'Welcome to Your Vue.js PWA',
    };
  },

  components: {
    DashboardProjects,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

</style>
