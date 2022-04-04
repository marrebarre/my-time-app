<template>
  <v-container class="content d-flex flex-wrap justify-center">
    <v-card elevation="8">
      <v-container>
        <v-col class="text-center">
          <v-text-field> Hey </v-text-field>
          <v-btn color="black">Hello</v-btn>
        </v-col>
      </v-container>
    </v-card>
    <v-card elevation="8"></v-card>
    <v-card elevation="8"></v-card>
    <v-card elevation="8"></v-card>
    <v-card elevation="8"></v-card>
    <v-card elevation="8"></v-card>
  </v-container>
</template>

<script>
export default {
  name: "HomePage",

  data: () => ({}),
};
</script>

<style scoped>
.content {
  height: 1000px;
}
.v-card {
  height: 400px;
  min-width: 500px;
  padding: 25px;
  margin: 25px;
  background-color: rgb(92, 86, 86);
}

.v-btn {
  text-transform: capitalize;
}
</style>
