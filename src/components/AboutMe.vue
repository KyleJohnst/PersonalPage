<template>
  <div v-if="viewMe">
    <h2 v-on:click="viewMe= false">About Me</h2>
    <div>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloremque veniam ducimus ipsa sunt odit, hic alias repudiandae officia commodi officiis placeat, sed quibusdam. Cumque quibusdam iure itaque quod! Soluta, illum.</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quaerat porro voluptates neque nulla magni, obcaecati dolor tempore id consectetur deleniti, officiis laudantium, earum deserunt? Voluptatum qui ex molestias explicabo aspernatur!</p>
    </div>
  </div>
</template>

<script>
import EventBus from "../Eventbus.js";

export default {
  name: "AboutMe",
  data() {
    return {
      viewMe: false
    };
  },
  mounted() {
    EventBus.$on("viewMe", () => {
      this.viewMe = true;
    });
  },
  methods: {}
};
</script>

<style>
</style>