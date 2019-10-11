<template>
  <div>
    <h3>Projects</h3>
    <div>Note:</div>

    <div
      style="color: #c5c6c7; padding-bottom: 10px"
    >Project names are links to their github repositories</div>
    <div class="skill_divider_bar"></div>
    <div v-for="(project, key) in projects" :key="key" class="proj_container">
      <div class="proj_left">
        <a :href="project.link" class="proj_header" target="_blank">
          <div>{{project.project_name}}</div>
        </a>
        <div class="proj_stack">{{project.stack}}</div>
      </div>
      <div class="proj_desc">{{project.description}}</div>
    </div>
    <div class="skill_divider_bar"></div>
    <div>
      <a class="proj_header" href="#top">Jump to top of page</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Projects",
  props: ["projects"]
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

.proj_link {
  text-decoration: none;
  color: #66fcf1;
}

.proj_link:hover {
  color: red;
  cursor: pointer;
}

.proj_header {
  padding-top: 10px;
  padding-bottom: 5px;
  font-weight: bold;
  text-decoration: none;
  color: #66fcf1;
}

.proj_header:hover {
  color: red;
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