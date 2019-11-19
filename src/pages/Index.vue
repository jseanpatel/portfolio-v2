<template>
  <Layout>
    <div id="landing" class="flex w-full h-screen bg-red-600">
      <div class="flex-1 w-1/6 bg-red-600">
        <navigation-bar>
          
        </navigation-bar>
      </div>
      <div class="flex-1 w-4/6 bg-red-600 text-center h-50%">
        <div class="bg-gray-400">
          <div class="object-contain h-48 w-full"></div>
        </div>
        <p class="text-white h-auto text-2xl font-sanspro content-center">
          <span class="font-semibold">Hi. </span>
          <span class="font-thin">My name is Jacob. I educate with code.</span>
        </p>
      </div>
      <div class="flex-1 w-1/6 bg-red-600"></div>
      <div class="bg-blue-600"></div>
    </div>
    <div class="justify-center allign-middle">
      <divider title="a little bit about me"> </divider>
    </div>
    <div id="about"></div>
    <div id="projects"></div>
    <div id="footer"></div>
  </Layout>
</template>

<script>
import TechnologyTag from "~/components/TechnologyTag.vue";
import Project from "~/components/Project.vue";
import NavigationBar from "~/components/NavigationBar.vue";
import Divider from "~/components/Divider.vue";

export default {
  components: {
    TechnologyTag,
    Project,
    NavigationBar,
    Divider
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
