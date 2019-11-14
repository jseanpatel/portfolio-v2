<template>
    <div class="bg-gray-500  inline-block px-5 rounded-lg">
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