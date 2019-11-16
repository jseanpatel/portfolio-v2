<template>
     <span> <p class="text-white h-auto text-2xl">  <span> {{title1}} </span> {{title2}} </p> </span>
</template>

<script>
export default {
  name: "LandingText",
  props: ["title1", "title2"],
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