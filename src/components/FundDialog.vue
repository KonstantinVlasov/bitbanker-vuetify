<template>
    <v-dialog
      v-model="dialog"
      persistent
      max-width="780"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="primary"
          v-bind="attrs"
          v-on="on"
          class="text-capitalize"
        >
          Fund my account
        </v-btn>
      </template>
      <v-card>
        <v-toolbar>
          <v-tabs v-model="tabs">
            <v-tab
              v-for="item in items"
              :key="item.tab"
              class="text-capitalize"
            >
              {{ item.tab}}
            </v-tab>
          </v-tabs>
          <v-btn
            icon
            @click="dialog = false"
          >
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-toolbar>
        <v-tabs-items v-model="tabs">
          <v-tab-item
            v-for="item in items"
            :key="item.tab"
          >
            <component
              v-bind:is="item.content"
              class="mt-8 mb-16"
              style="width: 380px"
            />
          </v-tab-item>
        </v-tabs-items>
      </v-card>
    </v-dialog>
</template>

<script>
import DepositForm from './DepositForm';
import WithdrawForm from './WithdrawForm';
import RebalanceForm from './RebalanceForm';

export default {
  name: 'FundForm',
  components: { DepositForm, WithdrawForm, RebalanceForm },
  data () {
    return {
      dialog: false,
      tabs: null,
      items: [{
        tab: 'Deposit', content: 'DepositForm'
      }, {
        tab: 'Withdraw', content: 'WithdrawForm'
      }, {
        tab: 'Rebalance', content: 'RebalanceForm'
      }]
    }
  }
}
</script>
