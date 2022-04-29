<template>
  <div>

    <div class="why">
      <div class="container">
        <div class="title">
          Why choose us?
        </div>
        <div class="slider mob">
          <div class="slider_wrap">
            <carousel v-if="!loading" :perPage="1" :paginationEnabled="false" :navigationEnabled="false">
              <slide>
                <div class="slider_item">
                  <img src="/images/why1.png" alt="">
                  <h3>Global Exposure</h3>
                  <span>Get access to 380k+ Biswap users <br>across the globe.</span>
                </div>
              </slide>
              <slide>
                <div class="slider_item">
                  <img src="/images/why2.png" alt="">
                  <h3>Liquidity</h3>
                  <span>Projects launched on Biswap <br>Launchpool will be listed and have high <br>trading liquidity.</span>
                </div>
              </slide>
              <slide>
                <div class="slider_item">
                  <img src="/images/why3.png" alt="">
                  <h3>Token Distribution</h3>
                  <span>Projects launched on Biswap <br>Launchpool will be listed and have high <br>trading liquidity.</span>
                </div>
              </slide>
              <slide>
                <div class="slider_item">
                  <img src="/images/why4.png" alt="">
                  <h3>Trading Competition</h3>
                  <span>Biswap will organize a tournament <br>dedicated to your project to maximize <br>trading volume with your token.</span>
                </div>
              </slide>
              <slide>
                <div class="slider_item">
                  <img src="/images/why5.png" alt="">
                  <h3>Marketing Boost</h3>
                  <span>Your project will be promoted across all <br>our social media platforms with an <br>audience of over 320K+.</span>
                </div>
              </slide>
              <slide>
                <div class="slider_item">
                  <img src="/images/why6.png" alt="">
                  <h3>Marketing Boost</h3>
                  <span>Your token might also be added to <br>Biswap Farms with high APR.</span>
                </div>
              </slide>
            </carousel>
          </div>
        </div>
        <div class="why_w pc-mob">
          <div class="wrap">
            <img src="/images/why1.svg" alt="">
            <h3>Global Exposure</h3>
            <span>Get access to 380k+ Biswap users <br>across the globe.</span>
          </div>
          <div class="wrap">
            <img src="/images/why2.svg" alt="">
            <h3>Liquidity</h3>
            <span>Projects launched on Biswap <br>Launchpool will be listed and have high <br>trading liquidity.</span>
          </div>
          <div class="wrap">
            <img src="/images/why3.svg" alt="">
            <h3>Token Distribution</h3>
            <span>Projects launched on Biswap <br>Launchpool will be listed and have high <br>trading liquidity.</span>
          </div>
          <div class="wrap">
            <img src="/images/why4.svg" alt="">
            <h3>Trading Competition</h3>
            <span>Biswap will organize a tournament <br>dedicated to your project to maximize <br>trading volume with your token.</span>
          </div>
          <div class="wrap">
            <img src="/images/why5.svg" alt="">
            <h3>Marketing Boost</h3>
            <span>Your project will be promoted across all <br>our social media platforms with an <br>audience of over 320K+.</span>
          </div>
          <div class="wrap">
            <img src="/images/why6.svg" alt="">
            <h3>Marketing Boost</h3>
            <span>Your token might also be added to <br>Biswap Farms with high APR.</span>
          </div>
        </div>
      </div>
    </div>

    <SelectToken />
  </div>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport';
import Helper from '~/components/Helper';
import SelectToken from '~/components/modals/SelectToken';


export default {
  data: () => ({
    loading: true,
    paggPadding: 5,
    flickityOptions: {
      initialIndex: 3,
      pageDots: true,
      wrapAround: true
    }
  }),
  mounted() {
    this.$nuxt.$emit('active-page', 1);
  },
  created() {
    this.$nextTick(function() {
      this.loading = false
    })
  },
  components:{
    SvgImport,
    Helper,
    SelectToken,
  }
}
</script>
