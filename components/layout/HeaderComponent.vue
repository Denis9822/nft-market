<template>
  <div>
  <header>
    <div @click="showSidebar(true)" class="sidebar_open mob">
      <SvgImport name="menu"/>
    </div>
    <a href="">
      <div class="header_market">
        <SvgImport name="money-tick"/>
        <span>Nft Market</span>
      </div>
    </a>
      <div class="header_right">
          <div class="certik">
            <img
              src="images/Certification.svg"
              width="89"
              height="24"
            />
          </div>

        <div @click="showModalWallet" class="btn_wallet">
          <SvgImport name="vuesax/bold/wallet-money"/>
          <span>Connect Wallet</span>
        </div>

      </div>

  </header>
    <ConnectWallet ref="modal"/>
  </div>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport'
import ConnectWallet from '~/components/modals/ConnectWallet';

export default {
  name: "HeaderComponent",
  methods:{
    showModalWallet(){
      this.$refs.modal.modalWallet = true;
    },
    showSidebar(arg){
      this.$nuxt.$emit('showSidebar', arg);
    }
  },
  created(){
    this.$nuxt.$on('showModalConnectWallet', data => {
      this.$refs.modal.modalWallet = true;
    })

  },
  components:{
    SvgImport,
    ConnectWallet,
  }
}


</script>

