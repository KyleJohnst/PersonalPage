<template>
  <div id="nav_bar">
    <div class="link_holder" v-on:click="navigateHandler('home')">Home</div>
    <div class="link_holder" v-on:click="navigateHandler('experience')">Experience</div>
    <div class="link_holder" v-on:click="navigateHandler('projects')">Projects</div>
    <div class="link_holder" v-on:click="navigateHandler('contact')">Contact</div>
  </div>
</template>

<script>
import EventBus from "../Eventbus.js";

export default {
  name: "NavBar",
  methods: {
    navigateHandler(choice) {
      EventBus.$emit("changeView", choice);
    }
  }
};
</script>

<style>
#nav_bar {
  display: flex;
  background-color: #0b0c1000;
  justify-content: center;
  margin: 0 14% 0 14%;
  padding: 2px 5px 0 5px;
}

.link_holder {
  background-color:#0b0c1000;
  border-bottom: 3px solid #0b0c1057;
  margin: 0 8px 0 8px;
  padding: 14px;
  color: #C5C6C7;
}

.link_holder:hover {
  border-bottom: 3px solid #45A29E;
  cursor: pointer;
}
</style>