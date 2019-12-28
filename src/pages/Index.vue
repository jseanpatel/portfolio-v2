<template>
  <Layout>
    <div id="landing" class="flex w-full h-screen bg-red-600">
      <div class="self-end flex-initial w-1/6 mb-12 bg-red-600">
        <navigation-bar></navigation-bar>
      </div>
      <div class="self-center flex-initial w-4/6 bg-red-600">
        <div
          class="flex justify-center h-auto text-2xl text-center text-white md:text-3xl lg:text-4xl md:text-left font-sanspro"
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
          class="self-center w-2/3 p-10 text-sm text-center bg-white rounded-lg lg:text-xl md:text-md md:p-16 sm:text-sm font-sanspro"
        >
          <p>I am a student at the University of California, Berkeley studying computer science.</p>
        </div>
      </div>
    </div>
    <divider class="justify-center align-middle" title="a collection of my projects"></divider>
    <div id="projects">
      <div class="flex w-full h-auto bg-backgroundGray">
        <div class="flex-row w-full h-auto">
          <div v-for="project in projects.projects" v-bind:key="project.name">
            <project :name="project.name" :description="project.description" :tags="project.tags"></project>
            <hr class="justify-center invisible border-gray-300 border-solid rounded-lg md:visible" />
          </div>
        </div>
      </div>
    </div>
    <divider class="justify-center align-middle" title="get in touch"></divider>
    <footer id="footer" class="w-full h-auto font-sanspro">
      <div class="flex h-auto bg-footerGray">
        <div class="w-1/6"></div>
        <div class="flex flex-col w-2/6 mr-3 md:mr-1 lg:mr-0">
          <p
            class="pt-12 text-lg font-bold text-white md:text-xl lg:text-2xl"
          >What am I currently working on?</p>
          <p
            class="pb-12 mt-4 text-sm font-normal text-white md:text-md lg:text-lg lg:mt-6"
          >I'm currently working on expanding my personal portfolio.</p>
        </div>
        <div
          class="flex flex-col w-2/6 max-w-sm pt-12 pl-0 text-lg font-bold text-white lg:ml-0 md:text-xl lg:text-2xl"
        >
          <div class="pl-4 -ml-4">Where am I heading next?</div>
          <p
            class="mt-4 text-sm font-normal text-white md:text-md lg:text-lg lg:mt-6"
          >Thai Basil in Berkeley. Check it out. It's really something special.</p>
        </div>
        <div class="w-1/6"></div>
      </div>
      <div class="flex justify-center h-auto bg-footerBlack">
        <div class="w-1/6"> </div>
        <div class="flex flex-row hidden w-1/6 md:flex">
          <div class="mt-24 text-xl font-bold text-white lg:text-2xl"> <span class="p-4 bg-red-600 rounded-lg"> Jacob Patel</span></div>
        </div>
        <div class="w-3/6">
          <p
            class="mt-20 text-xl font-extrabold text-white lg:text-2xl"
          >I work to bridge financial barriers and expand education to all; <span class="text-red-600">let's build something together.</span></p>
          <div class="flex flex-col mt-6 md:flex-row">
            <div
              class="flex font-semibold text-white lg:w-1/3 text-md"
            >Find me on social media:</div>
            <div
              class="flex items-center justify-between mt-4 text-sm font-normal text-white underline md:w-1/3 lg:-ml-4 md:justify-around md:mt-0"
            >
              <a href="https://github.com/jseanpatel">
                <font-awesome class="text-white fa-lg md:fa-2x" :icon="['fab', 'github']" />
              </a>
              <a href="https://twitter.com/">
                <font-awesome class="text-white fa-lg md:fa-2x" :icon="['fab', 'twitter']" />
              </a>
              <a href="https://www.linkedin.com/in/jseanpatel/">
                <font-awesome class="text-white fa-lg md:fa-2x" :icon="['fab', 'linkedin']" />
              </a>
              <a href="https://ko-fi.com/jseanpatel">
                <font-awesome class="text-white fa-lg md:fa-2x" :icon="['fas', 'coffee']" />
              </a>
            </div>
          </div>
          <div class="flex flex-col mt-2 md:flex-row">
            <div class="flex font-semibold text-white lg:w-1/3 text-md">Send me a message:</div>
            <div
              class="flex w-1/3 mt-2 font-normal text-white underline md:ml-4 lg:ml-0 md:mt-0 text-md" href="mailto:jseanpatel@berkeley.edu"
            >jseanpatel@berkeley.edu</div>
          </div>
          <div class="flex flex-col mt-2 md:flex-row">
            <div
              class="flex justify-start font-semibold text-white lg:w-1/3 text-md"
            >  Checkout out my resume: </div>
            <a href="Resume.pdf">
            <div
            > JacobPatelResume</div></a>

          </div>

          <div class="flex pt-40 pb-4 font-normal text-white text-md">
            <span>
            The source code of this website is licensed MIT and is available on Github.
            <a
              href="https://github.com/jseanpatel/Portfolio"
            >
              <font-awesome
                class="ml-0 text-white md:ml-1 sm:ml-4 fa-lg md:fa-2x"
                :icon="['fab', 'github']"
              />
            </a>
            </span>
          </div>
        </div>
      
      
      <div class="w-1/6">
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
