<template>
  <div>
    <h3>Contact Me</h3>
    <div class="divider_bar"></div>
    <div>
      <div class="contact_message">I'd love to hear from you, get in touch!</div>
      <div class="content_divider_bar"></div>
      <div class="contact_opt_container">
        <div class="contact_option">
          <a :href="`mailto:kyle9657@gmail.com`">
            <img class="contact_img" src="../../public/emailLogo.png" alt="image of email" />
          </a>
          <div>Email</div>
        </div>
        <div class="contact_option">
          <a href="https://www.linkedin.com/in/kylew-johnston/" target="_blank">
            <img class="contact_img" src="../../public/linkedIn.png" alt="linked in logo" />
          </a>
          <div>LinkedIn</div>
        </div>

                <div class="contact_option">
          <a href="https://github.com/KyleJohnst" target="_blank">
            <img class="contact_img" src="../../public/github.png" alt="github logo" />
          </a>
          <div>Github</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ContactMe"
};
</script>

<style>
.contact_opt_container {
  display: flex;
  justify-content: center;
}

.contact_option {
  display: inline-block;
  padding-left: 10px;
  padding-top: 10px;
  margin: 5px;
}

.content_divider_bar {
  border-bottom: 1px solid #45a29e;
  margin: 10px 30% 5px 30%;
}

.contact_message {
  color: #c5c6c7;
}

.contact_img {
  width: 110px;
  height: 100px;
}

.contact_img:hover{
    width: 120px;
  height: 110px;
}
</style>