<template>
  <v-app>
    <v-main class="py-8">
      <h1 class="text-center">Vuetify fund my account modal example</h1>
      <v-row justify="center" class="py-8">
        <FundDialog/>
      </v-row>
    </v-main>
  </v-app>
</template>

<script>
import FundDialog from './components/FundDialog';

export default {
  name: 'App',

  components: {
    FundDialog
  },

  data: () => ({
    //
  }),
};
</script>
