<template>
  <div class="wrap_main">
    <Preloader/>
    <SidebarComponent/>
    <div class="wrap">
      <div class="header_bg_red mob"></div>
      <div class="header_bg_green mob"></div>
      <HeaderComponent />
       <Support/>
      <nuxt/>
      <FooterComponent/>
    </div>
  </div>
</template>

<script>
import HeaderComponent from '~/components/layout/HeaderComponent';
import ConnectWallet from '~/components/modals/ConnectWallet';
import SidebarComponent from '~/components/layout/SidebarComponent';
import FooterComponent from '~/components/layout/FooterComponent';
import SvgImport from '~/components/layout/SvgImport';
import Support from '~/components/layout/Support';
import Preloader from '~/components/Preloader';
export default {
  head(){
    return{
      link:[
        {rel:"canonical",href: `http:localhost:3000${this.$route.path}`}
      ]
    };
  },
  methods:{

  },
  components:{
    HeaderComponent,
    SidebarComponent,
    SvgImport,
    FooterComponent,
    Support,
    ConnectWallet,
    Preloader,
  },
  name: "default"
}
</script>

