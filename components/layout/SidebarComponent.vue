<template>

  <div class="sidebar">
      <div class="sidebar_menu">
        <div class="sidebar_menu_item" :class="{sidebar_menu_active:page==1}">
          <NuxtLink to="/">
            <SvgImport name="vuesax/bold/home-2"/>
            <span>Home</span>
          </NuxtLink>
        </div>
        <div class="sidebar_menu_item" :class="{sidebar_menu_active:page==2}">
          <NuxtLink to="/swap">
            <SvgImport name="vuesax/bold/money-change"/>
            <span>Exchange</span>
          </NuxtLink>
        </div>
        <div class="sidebar_menu_item" :class="{sidebar_menu_active:page==3}">
          <NuxtLink to="/liquidity">
            <SvgImport name="vuesax/bold/dollar-circle"/>
            <span>Luquidity</span>
          </NuxtLink>
        </div>
        <div class="sidebar_menu_item" :class="{sidebar_menu_active:page==4}">
          <NuxtLink to="/farms">
            <SvgImport name="coin"/>
            <span>Farms</span>
          </NuxtLink>
        </div>
        <div @click="launchpool = !launchpool" class="sidebar_menu_item">
            <div class="sidebar_menu_item_with-levels" >
              <SvgImport name="ion/rocket"/>
              <span>Launchpools</span>
              <div class="arrow-down" :class="{menu_click:launchpool==true}" >
                <SvgImport name="Down"/>
              </div>
            </div>
            <div v-if="launchpool==true" class="sidebar_menu_item_hidden">
                <a href="" class="stake_active">Stake Bsw</a>
                <a href="" class="">Stake Tokens</a>
            </div>
        </div>
        <div class="sidebar_menu_item">
          <a class="" href="/">
            <SvgImport name="vuesax/bold/strongbox"/>
            <span>IDO</span>
          </a>
        </div>
        <div class="sidebar_menu_item sidebar_menu_item--style_yellow">
          <a class="" href="/">
            <SvgImport name="profile-2user"/>
            <span>Refferal program</span>
          </a>
        </div>
        <div class="sidebar_menu_item sidebar_menu_item--style_text">
          <a class="" href="/">
            <SvgImport name="vuesax/bold/ticket-star"/>
            <span>Lottery</span>
          </a>
          <div class="sidebar_menu_item_info">
             Win
          </div>
        </div>

      </div>
  </div>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport'

export default {
  name: "SidebarComponent",
  data: function () {
    return {
      page: 1,
      launchpool: false,
    }
  },
  created() {
    this.$nuxt.$on('active-page', data => {
      this.page = data;
    })
  },
  components:{
    SvgImport,
  }
}

</script>

