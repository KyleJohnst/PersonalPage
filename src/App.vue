<template>
  <div id="app">
    <div>
      <h1>Kyle Johnston</h1>
    </div>
      <nav-bar />
    
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
        {
          'name': 'C#',
          'img': 'https://cdn.iconscout.com/icon/free/png-256/c-sharp-2-569585.png'
        },
        {
          'name': 'Java',
          'img': 'https://cdn.iconscout.com/icon/free/png-256/java-43-569305.png'
          },
        {
          'name': 'React.JS',
          'img': 'https://cdn.iconscout.com/icon/free/png-256/react-4-1175110.png'
          },
        {
          'name': 'Vue.JS',
          'img': 'https://cdn.iconscout.com/icon/free/png-256/vue-282497.png'
          },
        {
          'name': 'Spring',
          'img': 'https://spring.io/img/homepage/icon-spring-framework.svg'
          },
        {
          'name': 'Node.JS',
          'img': 'https://cdn.iconscout.com/icon/free/png-256/node-js-3-1174937.png'
          },
        {
          'name': 'MongoDB',
          'img': 'https://cdn.iconscout.com/icon/free/png-256/mongodb-3-1175138.png'
          },
        {
          'name': 'PostgreSQL',
          'img': 'https://cdn.iconscout.com/icon/free/png-256/postgresql-9-1175120.png'
          },
        {
          'name': 'JavaScript',
          'img': 'https://cdn.iconscout.com/icon/free/png-256/javascript-23-1174949.png'
        },
        {
          'name': 'Git',
          'img': 'https://cdn.iconscout.com/icon/free/png-256/git-17-1175218.png'
          },
        {
          'name': 'RESTful routes',
          'img': 'https://cdn.iconscout.com/icon/premium/png-256-thumb/data-in-rest-1-1096809.png'
          },
        {
          'name': 'UX',
          'img': 'https://cdn.iconscout.com/icon/premium/png-256-thumb/ux-2-877450.png'
          },
        {
          'name': 'Selenium',
        'img': 'https://cdn.iconscout.com/icon/premium/png-256-thumb/selenium-2-570545.png'
        },
        {
          'name': 'API Design',
          'img': 'https://cdn.iconscout.com/icon/premium/png-256-thumb/api-1675146-1421517.png'
          }
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
