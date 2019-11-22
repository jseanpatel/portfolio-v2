<template>
    <div class="inline-block px-5 text-white bg-gray-700 rounded">
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