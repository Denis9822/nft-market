<template>
  <div>
    <Exchange
      page-active="2"
      h2="Make a Swap at No Cost"
      about="Earn high yields from transaction fees. <br> Learn how to add liquidity"
    />
  </div>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport'
import Exchange from '~/components/Exchange'
export default {
  mounted() {
    this.$nuxt.$emit('active-page', 3);
  },
  components:{
    SvgImport,
    Exchange,
  }
}
</script>
