<template>
  <Layout>
    <div id="landing" class="flex w-full h-screen bg-red-600">
      <div class="self-end flex-initial w-1/6 mb-12 bg-red-600">
        <navigation-bar></navigation-bar>
      </div>
      <div class="self-center flex-initial w-4/6 bg-red-600">
        <div class="flex justify-center h-auto text-4xl text-white font-sanspro">
          <p>
            <span class="font-semibold">Hi.&nbsp;</span>
            <span class="font-thin">My name is Jacob. I educate with code.</span>
          </p>
        </div>
      </div>

      <div class="flex-initial w-1/6 bg-red-600"></div>
      <div class></div>
    </div>
    <div id="divider" class="justify-center align-middle">
      <divider title="a little bit about me"></divider>
    </div>
    <div id="about">
      <div class="flex justify-center w-full h-screen bg-background_gray">
        <div
          class="self-center w-2/3 p-12 text-3xl text-center bg-white md:p-24 md:text-4xl h-half font-sanspro"
        >
          <p>I am a student at the University of California, Berkeley where I am studying computer science (BA)</p>
        </div>
      </div>
    </div>
    <div id="divider" class="justify-center align-middle">
      <divider title="a collection of my projects"></divider>
    </div>
    <div id="projects">
      <div class="flex w-full h-auto bg-background_gray">
        <div class="flex-row w-full h-auto">
          <div v-for="project in projects.projects" v-bind:key="project.project_name">
            <project
              :project_name="project.project_name"
              :project_description="project.project_description"
            ></project>
          </div>
        </div>
      </div>
    </div>
    <div id="divider" class="justify-center align-middle">
      <divider title="get in touch"></divider>
    </div>
    <div id="footer" class="flex-row w-full h-screen font-sanspro">
      <div class="flex-1 bg-footer_gray h-half">
        <div class="flex">
          <div class="flex w-1/6"></div>

          <div class="flex justify-end w-2/6">
            <div class="flex-row">
              <p class="pt-12 text-2xl font-bold text-white">What am I currently working on?</p>
              <p class="justify-end text-xl font-normal text-white">Right now I am working o</p>
            </div>
          </div>
          <div class="flex justify-start w-2/6 pt-12 text-2xl font-bold text-white">
            <div class="flex pl-4 ml-10">Where am I heading next?</div>
          </div>
          <div class="flex w-1/6"></div>
        </div>
      </div>
      <div class="flex-1 h-half bg-footer_black">
        <div class="flex">
          <div class="flex w-1/6"></div>
          <div class="flex w-1/6"></div>
          <div class="flex justify-start w-2/6 pt-12 text-2xl font-bold text-white">
            <div class="flex w-half">Hello</div>
            <div class="flex w-half">Hello</div>
          </div>
          <div class="flex w-1/6"></div>
          <div class="flex w-1/6"></div>
        </div>
      </div>
    </div>
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
