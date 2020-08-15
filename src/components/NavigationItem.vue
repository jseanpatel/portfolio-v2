<template>
  <a :href="href" class="font-light hover:underline">{{name}}</a>
</template>

<script>
import projects from "~/data/projects.json";

export default {
  name: "NavigationItem",
  props: ["name", "href"],
  data() {
    return {
      projects: projects,
    };
  },
  methods: {},
};
</script>

<style>
</style>