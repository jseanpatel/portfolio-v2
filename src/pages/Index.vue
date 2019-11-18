<template>
  <Layout>
    <div id="landing" class="flex w-full h-full absolute left-0 top-0 bg-red-600">
      <div class="flex-1 w-1/6 bg-red-600"></div>
      <div class="flex-1 w-4/6 bg-red-600 text-center h-50%">
         <p class="text-white h-auto text-2xl font-sanspro content-center">  <span class="font-semibold"> Hi. </span> <span class="font-thin"> My name is Jacob. I educate with code. </span> </p>
      </div>
      <div class="flex-1 w-1/6 bg-red-600"></div>
    </div>
    <div id="about"></div>
    <div id="projects"></div>
    <div id="footer"></div>
  </Layout>
</template>

<script>
import TechnologyTag from "~/components/TechnologyTag.vue";
import Project from "~/components/Project.vue";
import LandingText from "~/components/LandingText.vue";

export default {
  components: {
    TechnologyTag,
    Project,
    LandingText
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
