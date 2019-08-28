<template>
  <div>
  <div>
    <div>Languages Frameworks and such</div>
    <div>
    <div v-for="(skill, key) in skills" :key="key">{{skill.name}}</div>
    </div>
  </div>
  <div>
    <div>
      My Summary.
    </div>
    <div>
    <div>A highly driven individual with a keen interest in Tech and IT. A problem solver at heart I excel at being immersed in challenges and problems that force me out of my comfort zone. Ability to work across the Full Stack with a preference to Front End Development. Along with a varied background in customer services, hospitality, marketing and public relations.</div>
    </div>
  </div>
  <div>
    <div>
      Other things about me.
    </div>
    <div>
      <div>Bilingual in English and Afrikaans. Drivers Licence. Scuba Diver.</div>
    </div>
  </div>
  </div>
</template>

<script>
export default {
  name: "HomePage",
  props: ['skills']
};
</script>

<style>
</style>