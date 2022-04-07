<template>
  <div class="exchange_wrap">
    <div class="bg-exchange"></div>
    <div class="bg-ellipse-red"></div>
    <div class="bg-ellipse-green"></div>
    <div class="exchange">
      <h2>{{h2}}</h2>
      <h3 v-html="about"></h3>
      <div v-if="pageActive==1" class="q_w">
        <div class="quick_use">
          <div class="row">
            <div class="column">
              <div class="w">
                <span>Fee Return:</span>
                <p>0.000000 BSW</p>
              </div>
              <div class="help">
                <img src="/images/help.png" alt="">
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
              <div class="help right-m">
                <img src="/images/help.png" alt="">
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
        <div v-if="pageActive==1" class="swap">
          <div class="texts">
            <div class="column">
              <h4>Exchange</h4>
              <span>Trade tokens in an instant</span>
            </div>
            <SvgImport name="setting-2"/>
          </div>
          <div class="form_w">
            <div class="input_w">
              <input type="text" value="435342">
              <div class="coin_select">
                <img src="/icons/bnb.png" alt="">
                <span>BNB</span>
                <img src="/images/down.png" alt="">
              </div>
            </div>
            <div class="change">
              <img src="/images/Swipe.png" alt="">
            </div>
            <div class="input_w">
              <input type="text" value="435342">
              <div class="coin_select">
                <img src="/icons/bsw.png" alt="">
                <span>BSW</span>
                <img src="/images/down.png" alt="">
              </div>
            </div>
            <div class="btn">
              <SvgImport name="card-tick"/>
              <span>Unlock Wallet</span>
            </div>
          </div>
        </div>
        <div v-if="pageActive==2" class="liquidity">
          <div class="wrap" >
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
            <img src="/images/help-gray.png" alt="">
          </div>
          <div class="wallet">
            Connect a wallet to view your liquidity.
          </div>
          <div class="desc">
            Or, if you staked your LP tokens in a farm, unstake them to see them <br>here.
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport'

export default {
  props: {
    h2: { type: String, default: "" },
    about: { type: String, default: "" },
    pageActive: { type: Number, default: 0 },
  },
  name: "Support",
  components: {
    SvgImport,
  }
}


</script>

