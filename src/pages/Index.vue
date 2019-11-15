<template>
  <Layout>
    <div id="landing">
    </div>
    <div id="about">
    </div>
    <div id="projects">
    </div>
    <div id="footer">
    </div>
  </Layout>
</template>

<script>

import TechnologyTag from '~/components/TechnologyTag.vue'
import Project from '~/components/Project.vue'
import Landing from '~/components/Landing.vue'

export default {
  components: {
    TechnologyTag,
    Project,
    Landing
  },
  metaInfo: {
    title: 'Hello, world!'
  }
  
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
