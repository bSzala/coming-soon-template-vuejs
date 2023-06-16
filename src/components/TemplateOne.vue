<template>
  <b-row no-gutters class="h-100 template-one">
    <b-col
      cols="12"
      sm="6"
      xl="8"
      class="p-5 d-none d-sm-flex justify-content-center align-items-center background-container"
      :style="{ backgroundImage: 'url(' + backgroundImage + ')' }"
    ></b-col>
    <b-col
      cols="12"
      sm="6"
      xl="4"
      class="bg-light p-5 d-flex flex-column justify-content-center align-items-center shadow-lg"
    >
      <div class="text-center my-auto">
        <img :src="logo" alt="logo" class="img-fluid mx-auto mb-4" />
        <div class="title mb-3">{{ title }}</div>
        <div class="disclaimer font-weight-light">
          <vue-typed-js class="d-block" :loop="true" :strings="disclaimer">
            <span class="typing"></span>
          </vue-typed-js>
        </div>
      </div>
      <div class="mt-auto text-center social-media-container">
        <a
          href="https://www.linkedin.com/in/bszala"
          target="_blank"
          class="text-body mx-2 my-3"
          >LinkedIn</a
        >
      </div>
    </b-col>
  </b-row>
</template>

<script>
export default {
  name: "TemplateOne",
  data() {
    return {
      logo: require("@/assets/logo.png"),
      backgroundImage: require("@/assets/bg.jpg"),
      title: "Senior IT Consultant",
      disclaimer: [
        "Full Stack Developer",
        "Microservices",
        "Vue.js / Quasar / Vuetify",
        "Typescript / JavaScript / PHP",
        "Laravel",
        "SCRUM",
        "AWS",
        "GraphQL / AXIOS",
        "Rest API",
        "E-Commerce Solutions",
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.template-one {
  .title {
    font-size: 3rem;
  }
  .disclaimer {
    font-size: 1.5rem;
  }
  .background-container {
    background-position: center center;
    background-size: cover;
    box-shadow: inset 0rem 0rem 5rem rgba(0, 0, 0, 0.2) !important;
  }
  .social-media-container {
    a {
      transition: all 1s;
      &:hover {
        color: gray !important;
        text-decoration: none;
      }
    }
  }
}
</style>
