<template>
    <div class="flex h-12 w-full text-center text-white font-sanspro bg-gray-600">
      <div class="flex-1 bg-gray-600 self-center">
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