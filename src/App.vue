<template>
  <v-app>
      <Menu />
    <v-main>
      <Home />
    </v-main>
  </v-app>
</template>

<script>
import Home from "./components/Home.vue";
import Menu from "./components/Menu.vue";

export default {
  name: "App",

  components: {
    Home,
    Menu,
  },

  data: () => ({
    //
  }),
};
</script>

<style >
</style>