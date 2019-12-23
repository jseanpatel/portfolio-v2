<template>
  <Layout>
    <div id="landing" class="flex w-full h-screen bg-red-600">
      <div class="self-end flex-initial w-1/6 mb-12 bg-red-600">
        <navigation-bar></navigation-bar>
      </div>
      <div class="self-center flex-initial w-4/6 bg-red-600">
        <div class="flex justify-center h-auto text-4xl text-center text-white md:text-left font-sanspro">
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
        <div class="self-center w-2/3 p-10 text-xs text-center bg-white rounded-lg lg:text-lg md:text-md md:p-16 sm:text-sm font-sanspro">
          <p> Contrary to popular belief, Lorem Ipsum is not simply random text. It has roots in a piece of classical Latin literature from 45 BC, making it over 2000 years old. Richard McClintock, a Latin professor at Hampden-Sydney College in Virginia, looked up one of the more obscure Latin words, consectetur, from a Lorem Ipsum passage, and going through the cites of the word in classical literature, discovered the undoubtable source. Lorem Ipsum comes from sections 1.10.32 and 1.10.33 of "de Finibus Bonorum et Malorum" (The Extremes of Good and Evil) by Cicero, written in 45 BC. This book is a treatise on the theory of ethics, very popular during the Renaissance. The first line of Lorem Ipsum, "Lorem ipsum dolor sit amet..", comes from a line in section 1.10.32.

The standard chunk of Lorem Ipsum used since the 1500s is reproduced below for those interested. Sections 1.10.32 and 1.10.33 from "de Finibus Bonorum et Malorum" by Cicero are also reproduced in their exact original form, accompanied by English versions from the 1914 translation by H. Rackham. </p>
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
      <div class="flex bg-footerGray h-half">
        <div class="w-1/6"></div>
        <div class="flex flex-col w-2/6">
          <p class="pt-12 text-2xl font-bold text-white">
            What am I currently working on?
          </p>
          <p class="text-xl font-normal text-white">
            Right now I am working on completing this here Portfolio.
          </p>
        </div>
        <div class="flex w-2/6 pt-12 text-2xl font-bold text-white">
          <div class="pl-4 ml-10">Where am I heading next?</div>
        </div>
        <div class="w-1/6"></div>
      </div>
      <div class="flex bg-footerBlack h-half">
        <div class="w-1/6"></div>
        <div class="flex w-1/6"></div>
        <div class="flex justify-start w-2/6 pt-12 text-2xl font-bold text-white">
          <div class="flex w-half">Hello</div>
          <div class="flex w-half">Hello</div>
        </div>
        <div class="flex w-1/6"></div>
        <div class="w-1/6"></div>
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
