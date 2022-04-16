<template>
  <div>
    <Exchange
      page-active="1"
      h2="Make a Swap at No Cost"
      about="Fee reimbursement of up to 90% in BSW tokens, 10% is credited to your Robi Boost & Squid Energy. You can change the percentage."
    />
  </div>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport'
import Exchange from '~/components/Exchange'

export default {
  mounted() {
    this.$nuxt.$emit('active-page', 2);
  },
  components:{
    SvgImport,
    Exchange,
  }
}
</script>
