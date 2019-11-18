<template>
    <div id="landing" class="flex">
      <div class="flex-1 bg-red-600">
          {{title}}
      </div>
    </div>
</template>

<script>
export default {
   name: "NavigationBar",
  props: ['title'],
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