<template>
    <div class="flex w-full h-12 text-sm text-center text-white lg:text-md bg-dividerGray font-sanspro">
      <div class="self-center flex-1">
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