<template>
  <div id="app">
    <home-page />
    <div class>
      <p v-on:click="setViewMe()">About Me</p>
    </div>
    <about-me />
    <experience />
    <projects />
    <p v-on:click="test('contact')">Contact Me!</p>
    <contact-me v-if="contactView"/>
  </div>
</template>

<script>
import HomePage from "./components/HomePage.vue";
import AboutMe from "./components/AboutMe.vue";
import Projects from "./components/Projects.vue";
import Experience from "./components/Experience.vue";
import ContactMe from "./components/ContactMe.vue";
import EventBus from "./Eventbus.js";

export default {
  name: "app",
  components: {
    HomePage,
    AboutMe,
    ContactMe,
    Experience,
    Projects
  },
  data() {
    return {
      projectView: false,
      contactView: false,
      experienceView: false,
      AboutView: false
    };
  },
  methods: {
    setViewMe() {
      EventBus.$emit("viewMe");
    },
    test(view){
      if (view === 'contact') {
        this.contactView = true
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
</style>
