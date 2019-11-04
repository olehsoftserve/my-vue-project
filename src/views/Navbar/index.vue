<template>
  <nav>
    <v-app-bar flat app>
      <v-app-bar-nav-icon class="grey--text" @click="drawer = !drawer"></v-app-bar-nav-icon>
      <v-toolbar-title class="text-uppercase grey--text">
        <span class="font-weight-light">Em</span>
        <span class="lgcolor">Ocean</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn depressed color="grey--text">
        <span>Sign Out</span>
        <v-icon right>exit_to_app</v-icon>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer app v-model="drawer" class="blue lighten-3">
      <v-layout column align-center>
        <v-flex class="mt-5">
          <v-avatar size="100">
            <img src="https://scontent.flwo5-1.fna.fbcdn.net/v/t1.0-1/p160x160/69348205_2398932836867116_1130887459089940480_n.jpg?_nc_cat=101&_nc_oc=AQk7yvIC7h-1Pf89_-L02MxcSO5WxeVTrWtapPLFurJ887vbDRDhH0iWeROqK8-_6yM&_nc_ht=scontent.flwo5-1.fna&oh=72a52cb9d8e8b5836cc2a3bf1e14208e&oe=5E1D22E6" alt="cabinet_avatar">
          </v-avatar>
          <p class="white--text subheading mt-1">Oleh Kozhushko</p>
        </v-flex>
      </v-layout>
      <v-list>
        <v-list-item v-for="link in links" :key="link.text" router :to="link.route">
          <v-list-item-icon>
            <v-icon class="white--text">{{ link.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-content>
            <v-list-item-title class="white--text">{{ link.text }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      drawer: false,
      links: [
        { icon: "mdi-view-dashboard", text: "Dashboard", route: "/" },
        { icon: "mdi-folder", text: "Projects", route: "/projects" },
        { icon: "mdi-account", text: "Team", route: "/team" }
      ]
    };
  }
};
</script>

