<template>
  <header>
    <a href="">
      <div class="header_market">
        <SvgImport name="money-tick"/>
        <span>Nft Market</span>
      </div>
    </a>
      <div class="header_right">
          <div class="certik">
            <img
              src="images/Certification.png"
              width="89"
              height="24"
            />
          </div>
        <a href="">
        <div class="btn_wallet">
          <SvgImport name="vuesax/bold/wallet-money"/>
          <span>Connect Wallet</span>
        </div>
        </a>
      </div>
  </header>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport'

export default {
  name: "HeaderComponent",

  components:{
    SvgImport,
  }
}


</script>

