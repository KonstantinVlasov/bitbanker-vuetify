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

        <v-text-field
          label="Withdraw amount"
          solo flat
          background-color="border"
        >
          <v-chip
            slot="append"
            label
            color="label"
            class="white--text"
          >
            Max
          </v-chip>
        </v-text-field>

        <v-btn
          block
          large
          color="primary"
          class="text-capitalize"
        >
          Withdraw
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
