<template>
  <div class="flex-initial w-full h-56 bg-gray-100">
    <div class="flex justify-center w-full h-half ">
      <div class="flex self-center w-64 bg-gray-600 h-half">
        
      </div>
    </div>
    <div class="flex justify-center font-sanspro">
      <div class="flex-row text-center">
        <p class="text-3xl font-bold">{{project_name}}</p>
        <p class="text-xl">{{project_description}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Project",
  props: ["project_name", "project_description"],
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