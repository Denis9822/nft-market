<template>
  <div>
  <footer>
      <div class="container">
          <div class="wrap">
              <div class="stats">
                      <div class="coin">
                          <div class="row">
                              <img src="/images/coins/bsw.svg" alt="">
                            <div class="column">
                                <span>BSW</span>
                                <p>$0.691</p>
                            </div>
                          </div>
                          <div class="row">
                            <div class="meta">
                              <img src="/images/meta.svg" alt="">
                            </div>
                            <a href="">
                              <div class="btn_buy">
                               Buy BSW
                              </div>
                            </a>
                          </div>
                    </div>
                    <div class="info">
                        <div class="row">
                            <span>Max supply:</span>
                            <p>700 000 000</p>
                        </div>
                      <div class="row">
                        <span>Total supply:</span>
                        <p>252 932 688</p>
                      </div>
                      <div class="row">
                        <span>Circulating supply:</span>
                        <p>231 029 385</p>
                      </div>
                      <div class="row">
                        <span>Total Burned:</span>
                        <p>26 201 432</p>
                      </div>
                      <div class="row">
                        <span>Market Cap:</span>
                        <p>$154 746 659</p>
                      </div>
                    </div>
              </div>
              <div class="menu">
                  <div class="column" :class="{'links':statusShowItem[1] == true}">
                    <div class="wr">
                      <span>About</span>
                      <div class="mlauto" @click="showItem(1)" :class="{'hidden':statusShowItem[1] == false || statusShowItem[1] == undefined}">
                      <SvgImport name="minus"/>
                      </div>
                      <div class="mlauto" @click="showItem(1)" :class="{'hidden':statusShowItem[1] == true}" >
                      <SvgImport name="plus"/>
                      </div>
                    </div>
                    <a href="">Docs</a>
                    <a href="">Team</a>
                    <a href="">News</a>
                    <a href="">Github</a>
                    <a href="">Bug Bounty</a>
                  </div>
                <div class="column" :class="{'links':statusShowItem[2] == true}" >
                  <div class="wr">
                    <span>Products</span>
                    <div class="mlauto" @click="showItem(2)" :class="{'hidden':statusShowItem[2] == false || statusShowItem[2] == undefined}">
                      <SvgImport name="minus"/>
                    </div>
                    <div class="mlauto" @click="showItem(2)" :class="{'hidden':statusShowItem[2] == true}" >
                      <SvgImport name="plus"/>
                    </div>
                  </div>
                  <a href="">Exchange</a>
                  <a href="">Liquidity</a>
                  <a href="">Farms</a>
                  <a href="">Launchpools</a>
                  <a href="">Analytics</a>
                </div>
                <div class="column" :class="{'links':statusShowItem[3] == true}">
                  <div class="wr">
                    <span>Service</span>
                    <div class="mlauto" @click="showItem(3)" :class="{'hidden':statusShowItem[3] == false || statusShowItem[3] == undefined}">
                      <SvgImport name="minus"/>
                    </div>
                    <div class="mlauto" @click="showItem(3)" :class="{'hidden':statusShowItem[3] == true}" >
                      <SvgImport name="plus"/>
                    </div>
                  </div>
                  <a href="">Referral program</a>
                  <a href="">ESW Token</a>
                  <a href="">Apply to Launch</a>
                  <a href="">$10M Program</a>
                </div>
                <div class="column">
                  <div class="wr">
                    <span>Community</span>
                  </div>
                  <div class="social">
                      <div class="item">
                        <a href="">
                        <img src="/images/telegram.svg" alt="">
                        </a>
                      </div>
                    <div class="item">
                      <a href="">
                      <img src="/images/twitter.svg" alt="">
                      </a>
                    </div>
                    <div class="item">
                      <a href="">
                      <img src="/images/m.svg" alt="">
                      </a>
                    </div>
                    <div class="item">
                      <a href="">
                      <img src="/images/youtube.svg" alt="">
                      </a>
                    </div>
                  </div>
                </div>
              </div>
          </div>
      </div>
  </footer>
  </div>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport'

export default {
  name: "FooterComponent",
  data: () => ({
    statusShowItem: {},
  }),
  methods: {
    showItem(id) {
      if (this.statusShowItem[id]) {
        this.$set(this.statusShowItem, id, false);
      } else {
        this.$set(this.statusShowItem, id, true);
      }
    },
  },
  components:{
    SvgImport,
  }
}


</script>

