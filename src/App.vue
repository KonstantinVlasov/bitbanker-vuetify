<template>
  <v-app>
    <v-main>
      <FundDialog/>
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
