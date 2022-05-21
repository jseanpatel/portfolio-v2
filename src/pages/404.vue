<template>
  <Layout>
    <div class="flex w-full h-screen -mt-4 bg-green-700" id="landing">
      <div class="self-end flex-initial w-1/6 mb-12 bg-green-700">
        <div class="flex justify-center hidden lg:block">
          <div
            class="flex flex-col ml-16 text-lg text-center text-white lg:ml-0 md:text-xl lg:text-2xl font-sanspro"
          >
            <a href="/#about" class="font-bold hover:underline">about</a>
            <a href="/#projects" class="font-bold hover:underline">projects</a>
            <div
              class="flex-row w-full h-auto"
              v-for="project in projects.projects"
              v-bind:key="project.abbreviation"
            >
              <NavigationItem
                :name="project.abbreviation"
                :href="'/#' + project.abbreviation.replace(/\s/g, '')"
              ></NavigationItem>
            </div>
            <a href="/#blog" class="font-bold hover:underline">blog</a>
            <a href="/#contact" class="font-bold hover:underline">contact</a>
          </div>
        </div>
      </div>
      <div class="self-center flex-initial w-4/6 bg-green-700">
        <div
          class="flex flex-col h-auto text-3xl text-center text-white md:text-3xl lg:text-4xl md:text-left font-sanspro"
        >
        

          <p class="self-center">
            <span
              class="pr-1 text-5xl font-semibold transition duration-300 transformation-shadow"
              >404 - Page not found </span
            >
            
            </span>
          </p>
        </div>
      </div>

      <div class="w-1/6 bg-green-700"></div>
    </div>
    <divider
      class="justify-center w-full align-middle"
      id="about"
      title=""
    ></divider>
  
  
   
  </Layout>
</template>

<script>
import TechnologyTag from "~/components/TechnologyTag.vue";
import Project from "~/components/Project.vue";
import NavigationItem from "~/components/NavigationItem.vue";
import Divider from "~/components/Divider.vue";
import projects from "~/data/projects.json";


export default {
  components: {
    TechnologyTag,
    Project,
    NavigationItem,
    Divider,
  },
  metaInfo: {
    title: "Jacob Patel",
  },
  data() {
    return {
      projects: projects,
    };
  },
};
</script>


