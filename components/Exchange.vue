<template>
  <div class="exchange_wrap">
    <div class="bg-exchange"></div>
    <div class="bg-ellipse-red"></div>
    <div class="bg-ellipse-green"></div>
    <div class="exchange">
      <h2>{{ h2 }}</h2>
      <h3 v-html="about"></h3>
      <div v-if="pageActive==1" class="q_w">
        <div class="quick_use">
          <div class="row">
            <div class="column">
              <div class="w">
                <span>Fee Return:</span>
                <p>0.000000 BSW</p>
              </div>

            </div>
            <a href="">
              Withdraw
            </a>
          </div>
          <div class="row">
            <div class="column">
              <div class="w">
                <span>Robl Boost:</span>
                <p>0.00000 RB</p>
              </div>

            </div>
            <a href="">
              Use
            </a>
          </div>
        </div>
      </div>

      <div class="form">
        <div class="menu">
          <div @click="pageActive=1" class="item" :class="{active:pageActive==1}">
            Swap
          </div>
          <div @click="pageActive=2" class="item" :class="{active:pageActive==2}">
            Liquidity
          </div>
          <div @click="pageActive=3" class="item" :class="{active:pageActive==3}">
            Transactions
          </div>
        </div>

        <Swap :pageActive="pageActive" />
        <Liquidity :pageActive="pageActive" />
        <Transaction :pageActive="pageActive" />
      </div>
    </div>
    <SelectToken/>
    <ConnectWallet ref="modal"/>
  </div>

</template>

<script>
import SvgImport from '~/components/layout/SvgImport';
import Helper from '~/components/Helper';
import ConnectWallet from '~/components/modals/ConnectWallet';
import SelectToken from '~/components/modals/SelectToken';
import Swap from '~/components/exchange/Swap';
import Liquidity from '~/components/exchange/Liquidity';
import Transaction from '~/components/exchange/Transaction';
export default {
  props: {
    h2: {type: String, default: ""},
    about: {type: String, default: ""},
    pageActive: {type: String, default: 0},
  },
  data: function () {
    return {

    }
  },
  methods: {

  },
  name: "Support",
  components: {
    SvgImport,
    Helper,
    ConnectWallet,
    SelectToken,
    Swap,
    Liquidity,
    Transaction,
  }
}


</script>

