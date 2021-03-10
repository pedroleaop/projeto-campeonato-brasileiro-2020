<template>
  <v-app>
    <AppTopBar/>
  <v-main>
    <v-container>
      <router-view/>
    </v-container>
  </v-main>
  </v-app>
</template>

<script>
import AppTopBar from './components/shared/AppTopBar';

export default {
  name: 'App',

  components: {
    AppTopBar
  },

  data: () => ({
      drawer: false,
      group: null,
    }),
};
</script>
