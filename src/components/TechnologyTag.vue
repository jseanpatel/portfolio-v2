<template>
  <div class="inline-block px-3 my-1 text-sm text-white bg-gray-800 rounded md:px-4 lg:px-4">
    <p>{{title}}</p>
  </div>
</template>

<script>
export default {
  name: "TechnologyTag",
  props: ["title"],
  data() {
    return {
      message: "Try change me!"
    };
  },
  methods: {}
};
</script>

<style>
</style>