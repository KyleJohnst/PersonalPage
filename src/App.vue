<template>
  <div id="app">
    <a id="top"></a>
    <div>
      <h1>Kyle Johnston</h1>
    </div>
      <nav-bar />
    
    <div>
      <home-page v-if="homeView" :skills="skills"/>
      <experience v-if="experienceView" />
      <projects v-if="projectView" :projects="projects"/>
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
import skillsJson from "./resources/skills.json";
import projectsJson from "./resources/projects.json";

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
      skills: skillsJson,
      projects: projectsJson
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
  font-family: 'Archivo Narrow', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #66FCF1;
}

.divider_bar {
  border-bottom: 1px solid silver;
  margin: 0 28% 5px 28%;
}

body {
 background-color: #0b0c10e0;
}

h1 {
  font-size: 33px;
}
</style>
