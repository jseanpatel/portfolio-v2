<template>
  <div class="flex-col w-full h-auto p-2 duration-500 bg-gray-100" :id="id">
    <a :href="url">
      <div class="flex items-end justify-center">
        <!-- gridsome bug, address later https://github.com/gridsome/gridsome/issues/292 -->
        <g-image
          class="self-end w-24 p-2 mt-2 transition duration-200 ease-in-out transform bg-gray-200 border rounded-lg hover:scale-110"
          :src="require('!!assets-loader!~/assets/' + img)"
        />
      </div>
    </a>
    <div class="flex font-sanspro">
      <div class="flex-row hidden text-center md:w-1/3 md:block"></div>
      <div class="flex-row w-full text-center md:w-1/3">
        <p class="w-full pt-1 text-2xl font-bold md:text-2xl lg:text-3xl">{{name}}</p>
        <p class="hidden text-md md:text-lg lg:text-xl md:block">{{description}}</p>
        <div class="flex justify-center text-center lg:mx-0 md:hidden lg:flex-col">
          <div v-for="tag in tags">
            <technology-tag :title="tag"></technology-tag>
          </div>
        </div>
      </div>
      <div class="flex flex-row justify-start hidden w-auto ml-1 text-center md:block md:flex-col">
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
    TechnologyTag,
  },
  name: "Project",
  props: ["name", "description", "tags", "img", "url", "id"],
  data() {
    return {
      message: "Try change me!",
    };
  },
  methods: {
    buildImg() {
      return "@/assets/" + this.img;
    },
  },
};
</script>

<style>
</style>