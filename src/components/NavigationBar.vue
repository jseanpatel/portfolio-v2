<template>
  <div class="flex justify-center hidden md:block">
    <div
      class="flex flex-col ml-16 text-lg text-center text-white lg:ml-0 md:text-xl lg:text-2xl font-sanspro"
    >
      <a href="#about" class="font-bold hover:underline">about</a>
      <a href="#projects" class="font-bold hover:underline">projects</a>
      <a href="#flyright" class="font-light hover:underline">flyright</a>
      <a href="#" class="font-light hover:underline">maribel</a>
      <a href="#" class="font-light hover:underline">j2c</a>
      <a href="#" class="font-light hover:underline">ruhbl</a>
      <a href="#blog" class="font-bold hover:underline">blog</a>
      <a href="#contact" class="font-bold hover:underline">contact</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "NavigationBar",
  props: [],
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