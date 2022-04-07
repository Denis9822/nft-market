<template>
  <div>
  <footer>
      <div class="container">
          <div class="wrap">
              <div class="stats">
                      <div class="coin">
                          <div class="row">
                              <img src="/icons/bsw-full.png" alt="">
                            <div class="column">
                                <span>BSW</span>
                                <p>$0.691</p>
                            </div>
                          </div>
                          <div class="row">
                            <div class="meta">
                              <img src="/images/metamask.png" alt="">
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
                  <div class="column">
                    <span>About</span>
                    <a href="">Docs</a>
                    <a href="">Team</a>
                    <a href="">News</a>
                    <a href="">Github</a>
                    <a href="">Bug Bounty</a>
                  </div>
                <div class="column">
                  <span>Products</span>
                  <a href="">Exchange</a>
                  <a href="">Liquidity</a>
                  <a href="">Farms</a>
                  <a href="">Launchpools</a>
                  <a href="">Analytics</a>
                </div>
                <div class="column">
                  <span>Service</span>
                  <a href="">Referral program</a>
                  <a href="">ESW Token</a>
                  <a href="">Apply to Launch</a>
                  <a href="">$10M Program</a>
                </div>
                <div class="column">
                  <span>Community</span>
                  <div class="social">
                      <div class="item">
                        <a href="">
                        <img src="/images/telegram.png" alt="">
                        </a>
                      </div>
                    <div class="item">
                      <a href="">
                      <img src="/images/twitter.png" alt="">
                      </a>
                    </div>
                    <div class="item">
                      <a href="">
                      <img src="/images/m.png" alt="">
                      </a>
                    </div>
                    <div class="item">
                      <a href="">
                      <img src="/images/youtube.png" alt="">
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
  components:{
    SvgImport,
  }
}


</script>

