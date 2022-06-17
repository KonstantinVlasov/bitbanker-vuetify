<template>
  <v-container>
    <v-row justify="center">
      <v-col>
        <p class="text-caption">From</p>
        <v-select
          :items="exchanges"
          label="Choose exchange"
          solo flat
          background-color="border"
        ></v-select>

        <p class="text-caption">To</p>
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

        <p class="text-caption primary--text">
          You can transfer
          <v-chip
            slot="append"
            label
            small
            color="rgba(42, 101, 145, 0.1)"
            class="primary--text font-weight-bold"
          >
            1 246.64837562 SWZL (Swapzilla)
          </v-chip>
        </p>

        <v-menu offset-y>
          <template v-slot:activator="{ on, attrs }">
            <v-text-field
              label="Withdraw amount"
              solo flat
              background-color="border"
              v-bind="attrs"
              v-on="on"
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
          </template>
          <p>test</p>
        </v-menu>

        <v-checkbox
          label="Instant rebalance"
          class="mt-0"
        />

        <p class="text-caption primary--text">
          <span class="mr-8">Fee: <b>0.0004 SWZL</b></span>
          <span>Amount <b>with fee: 0 SWZL</b></span>
        </p>

        <v-btn
          block
          large
          color="primary"
          class="text-capitalize"
        >
          Apply
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
