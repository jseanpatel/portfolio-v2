<template>
    <div class="inline-block px-1 my-1 text-white bg-gray-800 rounded lg:px-5 ">
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