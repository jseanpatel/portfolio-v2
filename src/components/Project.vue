<template>
  <div class="flex-initial w-full h-56 bg-gray-100">
    <div class="flex justify-center w-full h-half">
      <div class="flex content-start self-center justify-center w-1/6">
        <!-- <hr class="justify-center invisible w-24 border-gray-500 border-solid rounded-lg md:visible"> -->
      </div>
      <div class="flex self-center w-4/6 bg-divder_gray">
        <!-- Image will be here. -->
      </div>
      <div class="flex content-start w-1/6"></div>
    </div>
    <div class="flex font-sanspro">
      <div class="flex-row hidden text-center md:w-1/3 md:block"></div>
      <div class="flex-row w-full text-center md:w-1/3">
        <p class="w-full text-2xl font-bold md:text-2xl lg:text-3xl">{{name}}</p>
        <p class="hidden text-md md:text-lg lg:text-xl md:block">{{description}}</p>
         <div class="flex flex-row justify-around mx-6 text-center lg:mx-0 md:hidden lg:flex-col">
        <div v-for="tag in tags">
          <technology-tag :title="tag"></technology-tag>
        </div>
      </div>
      </div>
      <div class="flex flex-row justify-start hidden w-auto text-center md:block md:flex-col">
        <div v-for="tag in tags">
          <technology-tag :title="tag"></technology-tag>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TechnologyTag from "~/components/TechnologyTag.vue";

export default {
  components: {
    TechnologyTag
  },
  name: "Project",
  props: ["name", "description", "tags"],
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