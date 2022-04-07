<template>
  <div class="wrap_main">
    <SidebarComponent/>
    <div class="wrap">
      <HeaderComponent/>
       <Support/>
      <nuxt/>
      <FooterComponent/>
    </div>
  </div>
</template>

<script>
import HeaderComponent from '~/components/layout/HeaderComponent';
import SidebarComponent from '~/components/layout/SidebarComponent';
import FooterComponent from '~/components/layout/FooterComponent';
import SvgImport from '~/components/layout/SvgImport';
import Support from '~/components/layout/Support'
export default {
  head(){
    return{
      link:[
        {rel:"canonical",href: `http:localhost:3000${this.$route.path}`}
      ]
    };
  },

  components:{
    HeaderComponent,
    SidebarComponent,
    SvgImport,
    FooterComponent,
    Support,
  },
  name: "default"
}
</script>

