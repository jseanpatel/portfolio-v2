<template>
  <div class="inline-block px-2 mx-1 my-1 text-xs text-white bg-gray-800 rounded sm:text-sm md:text-md md:px-3 lg:px-4">
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