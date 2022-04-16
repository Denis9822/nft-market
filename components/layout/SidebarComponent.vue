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
        <div @click="launchpool = !launchpool" class="sidebar_menu_item" :class="{sidebar_menu_active:page==5}">
            <div class="sidebar_menu_item_with-levels" >
              <SvgImport name="ion/rocket"/>
              <span>Launchpools</span>
              <div class="arrow-down" :class="{menu_click:launchpool==true||page==5}" >
                <SvgImport name="Down"/>
              </div>
            </div>
            <div v-if="launchpool==true||page==5" class="sidebar_menu_item_hidden">
              <NuxtLink to="/stake" class="stake_active">Stake Bsw</NuxtLink>
              <NuxtLink to="/stake" class="stake_active">Stake Tokens</NuxtLink>
            </div>
        </div>
        <div class="sidebar_menu_item" :class="{sidebar_menu_active:page==6}">
          <NuxtLink to="/ido">
            <SvgImport name="vuesax/bold/strongbox"/>
            <span>IDO</span>
          </NuxtLink>
        </div>
        <div class="sidebar_menu_item sidebar_menu_item--style_yellow" :class="{sidebar_menu_active:page==7}">
          <NuxtLink to="/refferal">
            <SvgImport name="profile-2user"/>
            <span>Refferal program</span>
          </NuxtLink>
        </div>
        <div class="sidebar_menu_item sidebar_menu_item--style_text" :class="{sidebar_menu_active:page==8}">
          <NuxtLink to="/lottery">
            <SvgImport name="vuesax/bold/ticket-star"/>
            <span>Lottery</span>
          </NuxtLink>
          <div class="sidebar_menu_item_info">
             Win
          </div>
        </div>

      </div>
  </div>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport'
import Helper from '~/components/Helper';
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
    Helper,
  }
}

</script>

