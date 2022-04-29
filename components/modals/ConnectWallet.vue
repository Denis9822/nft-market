<template>
  <div v-if="modalWallet" class="wall">
    <div class="wallet_wrap"></div>
  <div class="connect_wallet">
      <div class="title">
        <span>Connect wallet</span>
        <div @click="modalWallet = !modalWallet" class="close">
          <img src="/images/connectwallet-close.svg" alt="">
        </div>
      </div>
      <div class="wrap">
          <div class="item">
              <div class="img">
                <img src="/images/wallets/metamask.svg" alt="">
              </div>
              <span>Metamask</span>
          </div>
          <div class="item">
            <div class="img">
              <img src="/images/wallets/trust.svg" alt="">
            </div>
            <span>TrustWallet</span>
          </div>
        <div class="item">
          <div class="img">
            <img src="/images/wallets/walletconnect.svg" alt="">
          </div>
          <span>WalletConnect</span>
        </div>
        <div class="item">
          <div class="img">
            <img src="/images/wallets/pocket.svg" alt="">
          </div>
          <span>TokenPocket</span>
        </div>
        <div class="item">
          <div class="img">
            <img src="/images/wallets/math.svg" alt="">
          </div>
          <span>MathWallet</span>
        </div>
        <div class="item">
          <div class="img">
            <img src="/images/wallets/coin98.svg" alt="">
          </div>
          <span>Coin98</span>
        </div>
        <div class="item">
          <div class="img">
            <img src="/images/wallets/chain.svg" alt="">
          </div>
          <span>BinanceChain</span>
        </div>
        <div class="item">
          <div class="img">
            <img src="/images/wallets/safepal.svg" alt="">
          </div>
          <span>SafePal Wallet</span>
        </div>
        <div class="item">
          <div class="img">
            <img src="/images/wallets/coinbase.svg" alt="">
          </div>
          <span>Coinbase</span>
        </div>
        <div class="item">
          <div class="img">
            <img src="/images/wallets/huobi.svg" alt="">
          </div>
          <span>Huobi Wallet</span>
        </div>
      </div>
    <a href="">
      <div class="learn">
        <img src="/images/learn.svg" alt="">
        <span>Learn how to connect</span>
      </div>
    </a>
  </div>
  </div>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport';
import Helper from '~/components/Helper';
export default {
  props: {
  },
  data: function () {
    return {
      modalWallet: false,
    }
  },
  methods: {
  },
  name: "ConnectWallet",
  components: {
    SvgImport,
    Helper,
  }
}


</script>

