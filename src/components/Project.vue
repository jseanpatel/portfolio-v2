<template>
  <div class="flex-initial w-full h-56 bg-gray-100">
    <div class="flex justify-center w-full h-half">
      <div class="flex content-start self-center justify-center w-1/6">
       
      </div>
      <div class="flex self-center w-4/6 bg-divder_gray">
        <!-- Image will be here. -->
      </div>
      <div class="flex content-start w-1/6"></div>
    </div>
    <div class="flex justify-center font-sanspro">
      <div class="flex-row text-center">
        <p class="text-3xl font-bold">{{name}}</p>
        <p class="text-xl">{{description}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Project",
  props: ["name", "description"],
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