<template>
  <div>
    <h3>Experience</h3>
    <div class="divider_bar"></div>
    <div class="exp_container">
      <div class="exp_left">
      <div class="exp_header">Associate Automation Engineer</div>
      <div class="exp_comp">Verint Systems</div>
      <div class="exp_period">May 2019 - Current</div>
      </div>
      <div class="exp_desc">
        Develop actions using C# and selenium working in an agile environment, 
        to provide automated testing processes for QA teams various needs and specifications. 
        Leading team through learning fundamentals of React.js in weekly team Katas/training sessions.
      </div>
    </div>
    <div class="skill_divider_bar"></div>
    <div class="exp_container">
      <div class="exp_left">
      <div class="exp_header">Software Development Trainee</div>
      <div class="exp_comp">CodeClan Glasgow</div>
      <div class="exp_period">December 2018 - May 2019</div>
      </div>
      <div class="exp_desc">
        A 16 week, intensive course focusing on both Front End and Back End Web App development, 
        exposure to a variety of programming languages such as JavaScript, Java and Ruby. 
        Using Frameworks and Libraries such as Vue.js, React.js, Express.js, Spring, along with databases such as 
        Postgres SQL and MongoDB, API's, RESTful Routes. Developed using TDD, OOP, SOLID principals and BDD using 
        Agile Methodologies in solo, peer and mob programming environments.
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Experience"
};
</script>

<style>
.exp_container {
  display: flex;
  justify-content: space-evenly;
  margin: 0 4% 3% 4%;
}

.exp_left {
  display: inline-block;
  width: 20%;
}

.exp_header {
  padding-top: 10px;
  padding-bottom: 5px;
  font-weight: bold;
}

.exp_comp {
  padding-bottom: 5px;
  color:  #C5C6C7;
  font-weight: lighter;
}

.exp_period {
  padding-bottom: 5px;
  font-weight: lighter;
  width: 100%;
  color:  #C5C6C7;
}

.exp_desc {
  width: 80%;
  display: inline-block;
  padding-top: 20px;
  margin: 5px 5% 0 5%;
  color:  #C5C6C7;
}

.skill_divider_bar {
  border-bottom: 1px solid #45A29E;
  margin: 0 15% 5px 20%;
}

</style>