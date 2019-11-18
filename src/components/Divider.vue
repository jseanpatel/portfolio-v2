<template>
    <div class="flex h-10% w-full relative ">
      <div class="flex-1 bg-blue-600">
          {{title}}
      </div>
    </div>
</template>

<script>
export default {
   name: "Divider",
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