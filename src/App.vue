<template>
  <div id="app">
    <div>
      <h1>Kyle Johnston</h1>
    </div>
    <div>
      <nav-bar />
    </div>
    <div id="divider_bar"></div>
    <div>
      <home-page v-if="homeView" :skills="skills"/>
      <experience v-if="experienceView" />
      <projects v-if="projectView" />
      <contact-me v-if="contactView" />
    </div>
  </div>
</template>

<script>
import HomePage from "./components/HomePage.vue";
import Projects from "./components/Projects.vue";
import Experience from "./components/Experience.vue";
import ContactMe from "./components/ContactMe.vue";
import NavBar from "./components/NavBar.vue";
import EventBus from "./Eventbus.js";

export default {
  name: "app",
  components: {
    HomePage,
    ContactMe,
    Experience,
    Projects,
    NavBar
  },
  data() {
    return {
      homeView: true,
      projectView: false,
      contactView: false,
      experienceView: false,
      skills: [
        {'name': 'C#'},
        {'name': 'Java'},
        {'name': 'React.JS'},
        {'name': 'Vue.JS'},
        {'name': 'Spring'},
        {'name': 'Node.JS'},
        {'name': 'MongoDB'},
        {'name': 'PostgreSQL'},
        {'name': 'JavaScript'},
        {'name': 'Git/GitHub'},
        {'name': 'RESTful routes'}
        ]
      }
  },
  mounted() {
    EventBus.$on("changeView", choice => {
      this.viewSet(choice);
    });
  },
  methods: {
    viewSet(choice) {
      if (choice === "home") {
        this.projectView = false;
        this.contactView = false;
        this.experienceView = false;

        this.homeView = true;
      }
      if (choice === "experience") {
        this.projectView = false;
        this.contactView = false;
        this.experienceView = true;

        this.homeView = false;
      }
      if (choice === "projects") {
        this.projectView = true;
        this.contactView = false;
        this.experienceView = false;

        this.homeView = false;
      }
      if (choice === "contact") {
        this.projectView = false;
        this.contactView = true;
        this.experienceView = false;
        this.homeView = false;
      }
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#divider_bar {
  border: 1px, solid, black
}
</style>
