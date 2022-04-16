<template>
  <div v-if="modalWallet" class="connect_wallet">
      <div class="title">
        <span>Connect wallet</span>
        <div @click="modalWallet = !modalWallet" class="close">
          <img src="/images/connectwallet-close.png" alt="">
        </div>
      </div>
      <div class="wrap">
          <div class="item">
              <div class="img">
                <img src="/images/wallets/metamask.png" alt="">
              </div>
              <span>Metamask</span>
          </div>
          <div class="item">
            <div class="img">
              <img src="/images/wallets/trust.png" alt="">
            </div>
            <span>TrustWallet</span>
          </div>
        <div class="item">
          <div class="img">
            <img src="/images/wallets/walletconnect.png" alt="">
          </div>
          <span>WalletConnect</span>
        </div>
        <div class="item">
          <div class="img">
            <img src="/images/wallets/pocket.png" alt="">
          </div>
          <span>TokenPocket</span>
        </div>
        <div class="item">
          <div class="img">
            <img src="/images/wallets/math.png" alt="">
          </div>
          <span>MathWallet</span>
        </div>
        <div class="item">
          <div class="img">
            <img src="/images/wallets/coin98.png" alt="">
          </div>
          <span>Coin98</span>
        </div>
        <div class="item">
          <div class="img">
            <img src="/images/wallets/chain.png" alt="">
          </div>
          <span>BinanceChain</span>
        </div>
        <div class="item">
          <div class="img">
            <img src="/images/wallets/safepal.png" alt="">
          </div>
          <span>SafePal Wallet</span>
        </div>
        <div class="item">
          <div class="img">
            <img src="/images/wallets/coinbase.png" alt="">
          </div>
          <span>Coinbase</span>
        </div>
        <div class="item">
          <div class="img">
            <img src="/images/wallets/huobi.png" alt="">
          </div>
          <span>Huobi Wallet</span>
        </div>
      </div>
    <a href="">
      <div class="learn">
        <img src="/images/learn.png" alt="">
        <span>Learn how to connect</span>
      </div>
    </a>
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

