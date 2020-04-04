<template>
  <v-app>
    <v-navigation-drawer
      v-model="drawer"
      app
    >
      <Menu />
    </v-navigation-drawer>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content>
      <Top/>
    </v-content>
  </v-app>
</template>

<script>
import Menu from './views/Menu'
import Top from './views/Top'

export default {
  name: 'App',

  data: () => ({
      drawer: null,
    }),
    components: {
      Top,
      Menu,
    },
};
</script>
