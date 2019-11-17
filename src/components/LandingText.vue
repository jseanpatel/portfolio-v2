<template>
     <p class="text-white h-auto text-2xl font-sanspro content-center">  <span class="font-semibold"> {{title1}} </span> <span class="font-thin"> {{title2}} </span> </p>
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