<template>
  <Layout>
    <div id="landing" class="flex w-full h-screen bg-red-600">
      <div class="self-end flex-initial w-1/6 mb-16 bg-red-600">
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
    <div id="divider" class="justify-center allign-middle">
      <divider title="a little bit about me"></divider>
    </div>
    <div id="about">
      <div class="flex justify-center w-full h-screen bg-background_gray">
        <div
          class="flex self-center w-2/3 p-24 text-4xl font-normal text-center bg-white h-half font-sanspro"
        >
          <p>I am a student at the University of California, Berkeley where I am studying Computer Science (B.A.)</p>
        </div>
      </div>
    </div>
    <div id="divider" class="justify-center allign-middle">
      <divider title="a collection of my projects"></divider>
    </div>
    <div id="projects">
      <div class="flex w-full h-auto bg-background_gray">
        <div class="flex-row w-full h-auto">
          <div class="w-1/6 bg-black"></div>
          <div class="w-1/6 bg-black"></div>
          <div class="w-2/6 bg-black"></div>
          <div class="w-1/6 bg-black"></div>
          <div class="w-1/6 bg-black"></div>
          <!-- <project
            project_name="FlyRight: Space Adventure"
            project_description="A dangerous space adventure game."
          ></project>
          <div class="flex w-full h-0.2 text-white bg-gray-400 text-center font-sanspro"></div>
          <project
            project_name="Maribel - MLA Formatter"
            project_description="An all in one tool for formatting papers."
          ></project>
          <div class="flex w-full h-0.2 text-white bg-gray-400 text-center font-sanspro"></div>
          <project
            project_name="J2C - Jumpstart to College"
            project_description="A college date and deadline organizer."
          ></project>
          <div class="flex w-full h-0.2 text-white bg-gray-400 text-center font-sanspro"></div>
          <project
            project_name="RUHBL"
            project_description="The Redding United History Bowl League Website."
          ></project>-->
        </div>
      </div>
    </div>
    <div id="divider" class="justify-center allign-middle">
      <divider title="get in touch"></divider>
    </div>
    <div id="footer" class="flex-row w-full h-screen font-sanspro">
      <div class="flex-1 bg-footer_gray h-half"></div>
      <div class="flex-1 h-half bg-footer_black">
        <div class="flex justify-center">
          <p class="pt-12 text-2xl font-bold text-white">Contacts and Socials:</p>
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

export default {
  components: {
    TechnologyTag,
    Project,
    NavigationBar,
    Divider
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
