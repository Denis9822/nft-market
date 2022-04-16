<template>
  <div v-if="pageActive==3" class="transaction">
    <div class="wrap">
      <div class="texts">
        <div class="column">
          <h4>Recent transactions</h4>
          <span>Please connect your wallet to view your recent transactions</span>
        </div>
      </div>
      <div @click="showModalWallet" class="btn">
        <SvgImport name="vuesax/bold/wallet-money"/>
        <span>Connect Wallet</span>
      </div>
    </div>
  </div>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport';
import Helper from '~/components/Helper';
import SelectToken from '~/components/modals/SelectToken';
export default {
  props: {
    pageActive: {type: String, default: 0},
  },
  data: function () {
    return {

    }
  },
  methods: {
    showModalWallet(){
      this.$nuxt.$emit('showModalConnectWallet');
    }
  },
  mounted(){

  },
  name: "Liquidity",
  components: {
    SvgImport,
    Helper,
    SelectToken,
  }
}


</script>

