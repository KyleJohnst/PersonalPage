<template>
<div>
  <p v-on:click="navigateHandler('home')">Home</p>
    <p v-on:click="navigateHandler('experience')">Experience</p>
    <p v-on:click="navigateHandler('projects')">Projects</p>
    <p v-on:click="navigateHandler('contact')">Contact Me</p>
</div>
</template>

<script>
import EventBus from "../Eventbus.js";

export default {
  name: "NavBar",
  methods: {
    navigateHandler(choice){
      EventBus.$emit('changeView', choice);
    }
  }
};
</script>

<style>
</style>