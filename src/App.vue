<template>
  <v-app>
    <v-main>
      <Top />
      <Home />
    </v-main>
  </v-app>
</template>

<script>
import Home from "./components/Home.vue";
import Top from "./components/Top.vue";

export default {
  name: "App",

  components: {
    Home,
    Top,
  },

  data: () => ({
    //
  }),
};
</script>

<style scoped>
.v-application {
  background-color: rgb(112, 112, 112);
}
</style>