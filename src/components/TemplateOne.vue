<template>
  <b-row no-gutters class="h-100 template-one">
    <b-col
      cols="12"
      sm="6"
      xl="8"
      class="d-none d-sm-flex justify-content-center align-items-center background-container"
    >
      <video class="bg-video" autoplay muted loop>
        <source src="@/assets/header.mp4" type="video/mp4" />
        <source src="@/assets/header.webm" type="video/webm" />
        Your browser is not supported!
      </video>
    </b-col>
    <b-col
      cols="12"
      sm="6"
      xl="4"
      class="bg-light p-5 d-flex flex-column justify-content-center align-items-center shadow-lg"
    >
      <div class="text-center my-auto">
        <img :src="logo" alt="logo" class="img-fluid mx-auto mb-4" />
        <div class="title mt-2 mb-3">{{ title }}</div>
        <div class="title__small mb-3">{{ subtitle }}</div>
        <div class="disclaimer">
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
        <a
          href="mailto:info@vedevo.pl"
          target="_blank"
          class="text-body mx-2 my-3"
          >info@vedevo.pl</a
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
      title: "Bartłomiej Szala",
      subtitle: "Senior IT Consultant",
      disclaimer: [
        "Full Stack Developer",
        "Microservices",
        "Vue.js / Quasar / Vuetify / REACT / Laravel",
        "Typescript / JavaScript / PHP",
        "SCRUM",
        "Amazon AWS",
        "GraphQL / AXIOS",
        "Rest API",
        "E-Commerce Solutions",
        "Google FireBase",
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.bg-video {
  height: 100%;
  width: 100%;
  object-fit: cover;
  object-position: 2% bottom;
  filter: saturate(0%) blur(10px) brightness(130%);
}

.template-one {
  .title {
    text-align: center;
    font-size: 2.5rem;
    font-weight: 700;
    line-height: 2.5rem;
    &__small {
      font-size: 1.75rem;
      font-weight: 400;
      line-height: 2rem;
    }
  }
  .disclaimer {
    font-size: 1.25rem;
    font-weight: 400;
    color: #003566;
  }
  .background-container {
    background-position: center center;
    background-size: cover;
    box-shadow: inset 0rem 0rem 5rem rgba(0, 0, 0, 0.2) !important;
  }
  .social-media-container {
    & > a {
      transition: all 1s;
      font-weight: 700;
      &:hover {
        color: gray !important;
        text-decoration: none;
      }
    }
  }
}
</style>
