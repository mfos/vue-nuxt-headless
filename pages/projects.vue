<template>
  <div class="container">
    <section>
      <h1>projects</h1>
      <div v-for="project in githubProjects" :key="project.id">
        <h3><a :href="project.html_url">{{project.name}}</a></h3>
        <p>{{project.stargazers_count}}</p>
        <p>{{project.homepage}}</p>
        <p>{{project.description}}</p>
      </div>
      </section>

  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  computed: {
    ...mapState(["githubProjects"])
  },
  mounted() {
    this.$store.dispatch("getGithubProjects");
  }
}
</script>

<style lang="scss">
/* Sample `apply` at-rules with Tailwind CSS
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
