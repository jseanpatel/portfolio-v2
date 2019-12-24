<template>
  <Layout>
    <div id="landing" class="flex w-full h-screen bg-red-600">
      <div class="self-end flex-initial w-1/6 mb-12 bg-red-600">
        <navigation-bar></navigation-bar>
      </div>
      <div class="self-center flex-initial w-4/6 bg-red-600">
        <div
          class="flex justify-center h-auto text-4xl text-center text-white md:text-left font-sanspro"
        >
          <p>
            <span class="pr-1 font-semibold">Hi.</span>
            <span class="font-thin">My name is Jacob. I educate with code.</span>
          </p>
        </div>
      </div>

      <div class="flex-initial w-1/6 bg-red-600"></div>
      <div class></div>
    </div>
    <divider class="justify-center align-middle" title="a little bit about me"></divider>
    <div id="about">
      <div class="flex justify-center w-full py-32 bg-backgroundGray">
        <div
          class="self-center w-2/3 p-10 text-xs text-center bg-white rounded-lg lg:text-lg md:text-md md:p-16 sm:text-sm font-sanspro"
        >
          <p>I am a student at the University of California, Berkeley studying computer science.</p>
        </div>
      </div>
    </div>
    <divider class="justify-center align-middle" title="a collection of my projects"></divider>
    <div id="projects">
      <div class="flex hidden w-full h-auto bg-backgroundGray">
        <div class="flex-row w-full h-auto">
          <div v-for="project in projects.projects" v-bind:key="project.name">
            <project :name="project.name" :description="project.description" :tags="project.tags"></project>
            <hr class="justify-center invisible border-gray-300 border-solid rounded-lg md:visible" />
          </div>
        </div>
      </div>
    </div>
    <divider class="justify-center align-middle" title="get in touch"></divider>
    <footer id="footer" class="w-full h-screen font-sanspro">
      <div class="flex hidden bg-footerGray">
        <div class="w-1/6"></div>
        <div class="flex flex-col w-2/6">
          <p
            class="pt-12 text-lg font-bold text-white md:text-xl lg:text-2xl"
          >What am I currently working on?</p>
          <p
            class="mt-4 text-sm font-normal text-white md:text-md lg:text-lg lg:mt-6"
          >I am currently working on expanding my personal portfolio.</p>
          <p class="mt-4 text-sm font-normal text-white md:text-md lg:text-lg">
            You can check out my resume
            <span class="underline">here</span>.
          </p>
        </div>
        <div class="flex flex-col w-2/6 pt-12 text-2xl font-bold text-white">
          <div class="pl-4 -ml-4">Where am I heading next?</div>
          <p
            class="mt-4 text-sm font-normal text-white md:text-md lg:text-lg lg:mt-6"
          >Right now, I am running through the application process for 2020 summer internships.</p>
        </div>
        <div class="w-1/6"></div>
      </div>
      <div class="flex h-full bg-footerBlack">
        <div class="flex flex-row justify-center w-2/6"> <div class="mt-20 text-xl font-bold text-white"> Jacob Patel </div> 
        </div>
        <div class="w-4/6">
          <div
            class="flex justify-center w-4/6 mt-20 text-2xl font-normal font-extrabold text-white"
          >I work to bridge financial barriers and expand education to all; let's build something together.</div>
          <div class="flex flex-row mt-16">
            <div
              class="flex justify-start w-1/4 text-sm font-normal text-white"
            >Start a conversation:</div>
            <div
              class="flex justify-start w-1/4 text-sm font-normal text-white"
            >Other works: </div>
           
           <font-awesome class="text-white" :icon="['fab', 'github']"/>
           <font-awesome class="text-white" :icon="['fab', 'twitter']"/>
           <font-awesome class="text-white" :icon="['fab', 'Linkedin']"/>
           
          </div>
        <div class="flex flex-row mt-8">
            <div
              class="flex justify-start w-1/4 text-sm font-normal text-white underline"
            >jseanpatel@gmail.com</div>
            <div
              class="flex justify-start w-1/4 text-sm font-normal text-white underline"
            >https://maribel.io </div>
           
           <font-awesome class="text-white" :icon="['fab', 'github']"/>
           <font-awesome class="text-white" :icon="['fab', 'twitter']"/>
           <font-awesome class="text-white" :icon="['fab', 'Linkedin']"/>
           
          </div>
           
           
        
           
          </div>
        </div>
      </div>
    </footer>
  </Layout>
</template>

<script>
import TechnologyTag from "~/components/TechnologyTag.vue";
import Project from "~/components/Project.vue";
import NavigationBar from "~/components/NavigationBar.vue";
import Divider from "~/components/Divider.vue";
import projects from "~/data/projects.json";

export default {
  components: {
    TechnologyTag,
    Project,
    NavigationBar,
    Divider
  },
  metaInfo: {
    title: "Jacob Patel"
  },
  data() {
    return {
      projects: projects
    };
  }
};
</script>
