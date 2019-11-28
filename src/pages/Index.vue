<template>
  <Layout>
    <div id="landing" class="flex w-full h-screen bg-red-600">
      <div class="flex-initial w-1/6 bg-red-600 self-end mb-16">
        <navigation-bar></navigation-bar>
      </div>
      <div class="flex-initial w-4/6 bg-red-600 self-center">
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
    <div id="divider" class="justify-center allign-middle">
      <divider title="a little bit about me"></divider>
    </div>
    <div id="about">
      <div class="flex w-full h-screen bg-gray-300"></div>
    </div>
    <div id="divider" class="justify-center allign-middle">
      <divider title="a collection of my projects"></divider>
    </div>
    <div id="projects">
      <div class="flex w-full h-auto bg-gray-300">
        <div class="flex-row w-full h-auto">
        <project
          project_name="FlyRight: Space Adventure"
          project_description="A dangerous space adventure game."
        ></project>
        <project-divider>
        </project-divider>
        <project
          project_name="Maribel - MLA Formatter"
          project_description="An all in one tool for formatting papers."
        ></project>
        <project-divider>
        </project-divider>
        <project
          project_name="J2C - Jumpstart to College"
          project_description="A college date and deadline organizer."
        ></project>
         <project-divider>
        </project-divider>
        <project
          project_name="RUHBL"
          project_description="The Redding United History Bowl League Website."
        ></project>
        </div>
      </div>
    </div>
    <div id="divider" class="justify-center allign-middle">
      <divider title="get in touch"></divider>
    </div>
    <div id="footer" class="flex-row w-full h-screen bg-gray-700">
      <div class="flex-1 bg-gray-700 h-half"></div>
      <div class="flex-1 h-auto bg-black"></div>
    </div>
  </Layout>
</template>

<script>
import TechnologyTag from "~/components/TechnologyTag.vue";
import Project from "~/components/Project.vue";
import NavigationBar from "~/components/NavigationBar.vue";
import Divider from "~/components/Divider.vue";
import ProjectDivider from "~/components/ProjectDivider.vue";


export default {
  components: {
    TechnologyTag,
    Project,
    NavigationBar,
    Divider,
    ProjectDivider
  },
  metaInfo: {
    title: "Jacob Patel"
  }
};
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
