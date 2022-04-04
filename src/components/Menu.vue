<template>
  <div>
    <v-app-bar color="black" dense>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Marre</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-menu left bottom>
        <template v-slot:activator="{ on, attrs }">
          <v-btn icon v-bind="attrs" v-on="on">
            <v-icon>mdi-cog</v-icon>
          </v-btn>
        </template>
      </v-menu>
    </v-app-bar>
    <v-card class="mx-auto">
      <v-navigation-drawer
        v-model="drawer"
        color="grey-darken-4"
        dark
        temporary
      >
        <v-list color="grey-darken-4">
          <v-list-item
            v-for="item in items"
            :key="item.title"
            link
            @click="drawer = !drawer"
          >
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>

        <template v-slot:append>
          <div class="pa-2">
            <v-btn block color="black"> Logout </v-btn>
          </div>
        </template>
      </v-navigation-drawer>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "TopBar",
  data() {
    return {
      drawer: false,
      items: [
        { title: "Dashboard", icon: "mdi-view-dashboard" },
        { title: "Account", icon: "mdi-account-box" },
        { title: "Admin", icon: "mdi-gavel" },
      ],
    };
  },
};
</script>
