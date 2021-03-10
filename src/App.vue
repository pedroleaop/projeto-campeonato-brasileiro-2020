<template>
  <v-app>
    <AppTopBar/>
  <v-main>
    <v-container><Inicio/></v-container>
  </v-main>
  </v-app>
</template>

<script>
import Inicio from  './components/Inicio';
import AppTopBar from './components/shared/AppTopBar';

export default {
  name: 'App',

  components: {
    Inicio,
    AppTopBar
  },

  data: () => ({
      drawer: false,
      group: null,
    }),
};
</script>
