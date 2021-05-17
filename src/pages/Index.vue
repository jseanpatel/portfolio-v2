<template>
  <Layout>
    <div class="flex w-full h-screen -mt-4 bg-red-600" id="landing">
      <div class="self-end flex-initial w-1/6 mb-12 bg-red-600">
        <div class="flex justify-center hidden lg:block">
          <div
            class="flex flex-col ml-16 text-lg text-center text-white lg:ml-0 md:text-xl lg:text-2xl font-sanspro"
          >
            <a href="#about" class="font-bold hover:underline">about</a>
            <a href="#projects" class="font-bold hover:underline">projects</a>
            <div
              class="flex-row w-full h-auto"
              v-for="project in projects.projects"
              v-bind:key="project.abbreviation"
            >
              <NavigationItem
                :name="project.abbreviation"
                :href="'#' + project.abbreviation.replace(/\s/g, '')"
              ></NavigationItem>
            </div>
            <a href="#blog" class="font-bold hover:underline">blog</a>
            <a href="#contact" class="font-bold hover:underline">contact</a>
          </div>
        </div>
      </div>
      <div class="self-center flex-initial w-4/6 bg-red-600">
        <div
          class="flex flex-col h-auto text-3xl text-center text-white md:text-3xl lg:text-4xl md:text-left font-sanspro"
        >
          <img
            class="self-center w-56 h-56 sm:w-64 sm:h-64 mb-4 border rounded-full"
            alt="headshot"
            src="../assets/headshot.jpg"
          />

          <p class="self-center">
            <span class="pr-1 font-semibold transition duration-300 transformation-shadow">Hi.</span>
            <span class="font-thin">
              My name is Jacob.
              <span class="pr-1 font-semibold">I educate with code.</span>
            </span>
          </p>
        </div>
      </div>

      <div class="w-1/6 bg-red-600"></div>
    </div>
    <divider class="justify-center w-full align-middle" id="about" title="a little bit about me"></divider>
    <div>
      <div class="flex justify-center w-full py-32 bg-backgroundGray">
        <div
          class="self-center w-2/3 p-10 text-center bg-white rounded-lg text-md lg:text-xl md:text-lg md:p-16 sm:text-sm font-sanspro"
        >
          <p>I am an undergraduate at the University of California, Berkeley majoring in computer science and minoring in education. I am interested in using technology to bridge educational gaps that underrepresented groups face.</p>
        </div>
      </div>
    </div>
    <divider class="justify-center align-middle" id="projects" title="a collection of my projects"></divider>
    <div class="flex">
      <div class="flex-col w-full h-auto bg-backgroundGray">
        <div
          class="flex-row w-full h-auto"
          v-for="project in projects.projects"
          v-bind:key="project.name"
        >
          <project
            :name="project.name"
            :description="project.description"
            :id="project.abbreviation.replace(/\s/g, '')"
            :tags="project.tags"
            :img="project.img"
            :url="project.url"
          ></project>
          <hr class="justify-center invisible border-gray-300 border-solid rounded-lg md:visible" />
        </div>
      </div>
    </div>
    <divider class="justify-center align-middle" id="blog" title="get in touch"></divider>
    <footer class="w-full h-auto font-sanspro" id="footer">
      <div class="flex h-auto bg-footerGray">
        <div class="w-1/6"></div>
        <div class="flex flex-col w-2/6 pt-12 mx-2 lg:mr-0">
          <p
            class="text-lg font-bold text-white md:text-xl lg:text-2xl"
          >What am I currently building?</p>
          <p
            class="pb-12 mt-4 text-sm font-normal text-white md:text-md lg:text-lg lg:mt-6"
          >I'm currently working on expanding my freelance website design business called <a class="underline" href="https://ladderdesigns.com">
 Ladder Designs</a>.</p>
        </div>
        <div class="flex flex-col w-2/6 pt-12 pb-12 mx-4 text-lg">
          <div class="text-lg font-bold text-white md:text-xl lg:text-2xl">Where am I heading next?</div>
          <p
            class="mt-4 text-sm font-normal text-white md:text-md lg:text-lg lg:mt-6"
          >I'm about to start a SWE internship with Redfin. Throughout the summer I'll be working in the frontend with the Home Services team.</p>
        </div>
        <div class="w-1/6"></div>
      </div>
      <div class="flex justify-start h-auto bg-footerBlack">
        <div class="w-1/6"></div>
        <div class="flex flex-row hidden w-1/6 lg:flex">
          <div class="mt-24 text-xl font-bold text-white lg:text-2xl">
            <span class="p-4 bg-red-600 rounded-lg">Jacob Patel</span>
          </div>
        </div>
        <div id="contact" class="w-4/6 lg:w-3/6">
          <p class="mt-20 text-xl font-extrabold text-white lg:text-2xl">
            I work to bridge financial barriers and expand education to all.
            <span
              class="text-red-600"
            >Let's build something together.</span>
          </p>
          <div class="flex flex-row mt-6">
            <div
              class="flex flex-initial hidden w-auto font-semibold text-white md:block text-md md:text-md"
              ref="hello"
            >Find me on social media:</div>
            <div
              class="flex flex-initial block w-auto font-semibold text-white md:hidden text-md md:text-md"
            >Social media:</div>
            <div
              class="flex flex-row items-center justify-around w-1/2 ml-3 text-sm font-normal text-white underline sm:w-1/3 md:w-1/4 lg:w-1/4 md:mt-0"
            >
              <a href="https://github.com/jseanpatel">
                <font-awesome class="text-white fa-lg md:fa-2x" :icon="['fab', 'github']" />
              </a>
              <a href="https://twitter.com/jseanpatel">
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
          <div class="flex flex-row mt-2 overflow-auto">
            <div class="flex w-auto font-semibold text-white text-md lg:w-auto">Send me a message:</div>
            <div
              class="flex block w-auto ml-3 font-normal text-white underline md:hidden text-md overflow lg:w-auto"
              href="https://mail.google.com/mail/?view=cm&fs=1&tf=1&to=jseanpatel@gmail.com"
              target="_blank"
            >email</div>
            <a
              class="flex hidden w-auto ml-3 font-normal text-white underline md:block text-md overflow lg:w-auto"
              href="mailto:jseanpatel@berkeley.edu"
              target="_blank"
            >jseanpatel@berkeley.edu</a>
          </div>

          <div class="flex flex-row mt-2">
            <div
              class="flex justify-start w-auto font-semibold text-white text-md sm:text-md"
            >Checkout out my resume:</div>
            <a href="https://drive.google.com/open?id=1zn7AY7H7qoi3dBHJk6UciWDOOvsibOyN">
              <div
                class="flex w-auto ml-3 font-normal text-white underline md:ml-4 md:mt-0 text-md"
              >resume</div>
            </a>
          </div>

          <div class="flex pt-40 pb-4 font-normal text-white text-md">
            <span>
              The source code of this website is licensed MIT and is available on Github.
              <a
                href="https://github.com/jseanpatel/Portfolio"
              >
                <font-awesome
                  class="ml-0 text-white md:ml-1 fa-lg md:fa-2x"
                  :icon="['fab', 'github']"
                />
              </a>
            </span>
          </div>
        </div>
        <div class="hidden lg:w-1/6 lg:block"></div>
      </div>
    </footer>
  </Layout>
</template>

<script>
import TechnologyTag from "~/components/TechnologyTag.vue";
import Project from "~/components/Project.vue";
import NavigationItem from "~/components/NavigationItem.vue";
import Divider from "~/components/Divider.vue";
import projects from "~/data/projects.json";

const scrollDown = (location) => {
  target = document.getElementByID("location");
  target.scrollIntoView({ behavior: "smooth", alignToTop: false });
};

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


