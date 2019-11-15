<template>
    <div class="bg-gray-600  inline-block px-5 rounded-lg text-white">
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