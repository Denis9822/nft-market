<template>
  <div v-if="pageActive==2" class="liquidity">
    <div class="wrap">
      <div class="texts">
        <div class="column">
          <h4>Liquidity</h4>
          <span>Add liquidity to receive LP tokens</span>
        </div>
        <SvgImport name="setting-2"/>
      </div>
      <div class="btn">
        <SvgImport name="money-send"/>
        <span>Add Liquidity</span>
      </div>
    </div>
    <div class="row">
      <span>Your Liquidity</span>
      <Helper typeImg="1" nameImg="help-gray.png" />
    </div>
    <div class="wallet">
      Connect a wallet to view your liquidity.
    </div>
    <div class="desc">
      Or, if you staked your LP tokens in a farm, unstake them to see them <br>here.
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

