<template>
  <div>
    <h3>About Me</h3>
    <div class="divider_bar"></div>
    <div class="header">Overview</div>
    <div class="content_container">
      <div class="content">
        Im a highly driven individual with a keen interest in Tech and IT.
        As a problem solver at heart I excel at being immersed in challenges and problems that force me out of my comfort zone.
        Ability to work across the Full Stack with a preference to Front End Development.
        Along with a varied background in customer services, hospitality, marketing and public relations.
      </div>
    </div>
    <div>
      <div class="header">Technical Skills</div>
      <div class="section-content-grid">
        <div v-for="(skill, key) in skills" :key="key" class="grid-item">
          <div class="skill_box"><img class="skill_img" v-if="skill.img"  :src="skill.img" alt="">{{skill.name}}</div>
        </div>
      </div>
    </div>
    <div>
      <div class="header">More Info!</div>
      <div class="content_container">
        <div class="content">Bilingual in English and Afrikaans. Full Drivers Licence. Avid tech Scuba Diver. Arial Photographer</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomePage",
  props: ["skills"]
};
</script>

<style>
.header {
  margin: 10px 38% 10px 38%;
  padding-bottom: 5px;
  border-bottom: 1px solid #45A29E;
}

.content_container {
  display: flex;
  justify-content: center;
  margin: 0 20% 0 20%;
  padding: 5px;
  color: #C5C6C7;
}

.content {
  padding: 5px 5px 15px 5px;
}

/* Skills css */
.section-content-grid {
  margin-bottom: 25px;
}

.grid-item {
  padding-right: 5px;
  display: inline-block;
}

.skill_box {
  display: block;
  color:  #C5C6C7;
  margin-top: 5px;
  padding: 5px;
  border: 1px solid #45A29E;
}

.skill_img {
  width: 15px;
  height: 15px;
  padding-right: 2px;
}
</style>