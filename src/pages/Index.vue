<template>
  <Layout>
    <div id="landing" class="flex w-full h-full absolute left-0 top-0 bg-red-600">
      <div class="w-1/6 bg-red-600"></div>
      <div class="w-4/6 bg-red-600"></div>
      <div class="w-1/6 bg-red-600"></div>
    </div>
    <div id="about"></div>
    <div id="projects"></div>
    <div id="footer"></div>
  </Layout>
</template>

<script>
import TechnologyTag from "~/components/TechnologyTag.vue";
import Project from "~/components/Project.vue";
import Landing from "~/components/Landing.vue";

export default {
  components: {
    TechnologyTag,
    Project,
    Landing
  },
  metaInfo: {
    title: "Jacob Patel"
  }
};
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
