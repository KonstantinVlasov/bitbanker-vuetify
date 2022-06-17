<template>
  <v-container>
    <v-row justify="center">
      <v-col>
        <v-select
          :items="exchanges"
          label="Choose exchange"
          solo flat
          background-color="border"
        ></v-select>

        <v-select
          :items="currencies"
          label="Choose currency"
          solo flat
          background-color="border"
        ></v-select>

        <v-img
          :src="require('../assets/qrcode_tradopro.png')"
          max-height="120"
          max-width="120"
          class="mx-auto mt-4 mb-8"
        ></v-img>
        <p class="text-center mb-8">
          FGBfvcnkfdnvkk74365832ybvcvdfvfvb
        </p>

        <v-btn
          block
          large
          color="primary"
          class="text-capitalize"
        >
          Copy
        </v-btn>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      exchanges: [{
        text: 'Binance', value: 'binance'
      }, {
        text: 'Coinbase', value: 'coinbase'
      }, {
        text: 'Kraken', value: 'kraken'
      }, {
        text: 'FTX', value: 'ftx'
      }],
      currencies: [{
        text: 'Рубли', value: 'rub'
      }, {
        text: 'Доллары', value: 'ysd'
      }]
    }
  }
}
</script>
