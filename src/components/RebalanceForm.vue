<template>
  <v-container>
    <v-row justify="center">
      <v-col>
        <p class="text-caption mb-1 ml-4">From</p>
        <v-select
          :items="exchanges"
          label="Choose exchange"
          solo flat
          background-color="border"
        ></v-select>

        <p class="text-caption mb-1 ml-4">To</p>
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

        <p class="text-xs primary--text">
          You can transfer
          <v-chip
            slot="append"
            label
            x-small
            color="rgba(42, 101, 145, 0.1)"
            class="px-1 primary--text font-weight-bold"
          >
            1 246.64837562 SWZL (Swapzilla)
          </v-chip>
        </p>

        <v-menu offset-y nudge-bottom="-28">
          <template v-slot:activator="{ on, attrs }">
            <v-text-field
              label="Withdraw amount"
              solo flat
              background-color="border"
              v-bind="attrs"
              v-on="on"
            >
            </v-text-field>
          </template>
          <v-card class="py-2">
            <v-list-item>
              <v-chip
                label
                color="rgba(42, 101, 145, 0.1)"
                class="primary--text"
              >
                Balance:&nbsp;
                <span class="font-weight-bold">
                  0.04763864
                </span>
              </v-chip>
            </v-list-item>
            <v-list-item>
              <v-chip
                v-for="part in parts"
                :key="part"
                label
                color="label"
                class="white--text mr-2"
              >
                {{ part }}
              </v-chip>
            </v-list-item>
          </v-card>
        </v-menu>

        <v-checkbox
          label="Instant rebalance"
          class="mt-0"
        />

        <p class="text-xs primary--text">
          <span class="mr-8">Fee: <b>0.0004 SWZL</b></span>
          <span>Amount with fee: <b>0 SWZL</b></span>
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
      }],
      parts: ['10%', '25%', '50%', '100%', 'Split']
    }
  }
}
</script>
