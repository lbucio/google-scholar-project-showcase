<template>
  <div class="project">
      <h2 class="title">{{ project.name }}</h2>
      <h3 class="subtitle">{{ project.author }}</h3>
  </div>
</template>

<script>
export default {

  props: {
    project: {
      type: Object,
    },
  },

};
</script>

<style lang="scss">

.project {
  display: flex;
  flex-flow: column nowrap;
  text-align: left;

  width: 50%;
  padding: 5px;
  background-color: red;

  .title {
    margin-top: 0;
  }
}


</style>
