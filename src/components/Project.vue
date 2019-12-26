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
      <div class="flex-row w-1/3 text-center"></div>
      <div class="flex-row w-1/3 text-center">
        <p class="w-full text-xl font-bold lg:text-3xl">{{name}}</p>
        <p class="invisible hidden text-xl lg:visible">{{description}}</p>
         <div class="flex flex-row justify-center text-center lg:flex-col">
        <div v-for="tag in tags">
          <technology-tag :title="tag"></technology-tag>
        </div>
      </div>
      </div>
      <div class="flex flex-row justify-center hidden w-1/3 text-center lg:flex-col">
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