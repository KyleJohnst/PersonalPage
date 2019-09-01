<template>
  <div>
    <h3>Projects</h3>
    <div class="divider_bar"></div>
    <div>
      <div class="proj_container">
        <div class="proj_left">
          <div class="proj_header">Dive Tracker</div>
          <div class="proj_stack">
            Java, Spring,
            Postgres SQL, React,
            Hibernate, RESTful
            API, React-google-charts
          </div>
        </div>
        <div class="proj_desc">
          Personal project to create a web app to track and store dives.
          Includes graphs for dive visulisation and
          world maps showing all different sites. On going development
        </div>
      </div>

      <div class="skill_divider_bar"></div>

      <div class="proj_container">
        <div class="proj_left">
          <div class="proj_header">Hotel Manager</div>
          <div class="proj_stack">
            Java, Spring,
            Postgres SQL, React,
            Hibernate, RESTful
            API
          </div>
        </div>
        <div class="proj_desc">
          Group project Web App over 5 days to build a functional Hotel Management system,
          that allows the user to Create bookings with relational
          java models storing them in an SQL database.
        </div>
      </div>

      <div class="skill_divider_bar"></div>

      <div class="proj_container">
        <div class="proj_left">
          <div class="proj_header">Discord ChatBot</div>
          <div class="proj_stack">Node.JS, Discord.io, Discord</div>
        </div>
        <div
          class="proj_desc"
        >Simple chat bot that plays Rock, Paper, Scissors, Lizard, Spock that interacts with discord server users. Hosted on Heroku.</div>
      </div>

      <div class="skill_divider_bar"></div>

      <div class="proj_container">
        <div class="proj_left">
          <div class="proj_header">Remote Jobs Site</div>
          <div class="proj_stack">Express.JS, Vue.JS, External API, VueDraggable.</div>
        </div>
        <div class="proj_desc">Remote jobs board fetching recently posted jobs on an external API
           and hosted on Heroku.
           </div>
      </div>

      <div class="skill_divider_bar"></div>

      <div class="proj_container">
        <div class="proj_left">
          <div class="proj_header">Portfolio Site</div>
          <div class="proj_stack">Vue.JS</div>
        </div>
        <div class="proj_desc">Personal portfolio website, this site.</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Projects"
};
</script>

<style>
.proj_container {
  display: flex;
  justify-content: space-evenly;
  margin: 0 4% 3% 4%;
}

.proj_left {
  display: inline-block;
  width: 20%;
}

.proj_header {
  padding-top: 10px;
  padding-bottom: 5px;
  font-weight: bold;
}

.proj_stack {
  padding-bottom: 5px;
  color: #c5c6c7;
  font-weight: lighter;
}

.proj_desc {
  width: 80%;
  display: inline-block;
  padding-top: 20px;
  margin: 5px 5% 0 5%;
  color: #c5c6c7;
}

.proj_divider_bar {
  border-bottom: 1px solid #45a29e;
  margin: 0 25% 5px 25%;
}
</style>