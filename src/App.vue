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
      <v-toolbar-title>Takeout Hamamatsu</v-toolbar-title>
    </v-app-bar>

    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
import Menu from './views/Menu'

export default {
  name: 'App',

  data: () => ({
      drawer: null,
    }),
    components: {
      Menu,
    },
};
</script>