<template>
  <div id="app" class="overflow-x-hidden h-100">
    <template-one></template-one>
  </div>
</template>

<script>
import TemplateOne from "./components/TemplateOne.vue";

export default {
  name: "App",
  components: {
    TemplateOne,
  },
};
</script>

<style lang="scss" scoped>
#app {
  font-family: "Roboto", sans-serif;

  color: #001d3d;
}
</style>
