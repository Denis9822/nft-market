<template>
  <div class="launchpool">
      <div class="main">
          <div class="bg-ellipse-red"></div>
          <div class="bg-ellipse-green"></div>
          <div class="container">
            <div class="column">
                <h1>Launchpools</h1>
                <h2>
                  Looking for a less resource-intensive alternative to mining? <br>Use your BSW tokens to earn more tokens, for Free.
                </h2>
                <h4>Learn how to start</h4>
              <a href="">
                <div class="add">
                  <span>Add project</span>
                  <img src="/images/plus.png" alt="">
                </div>
              </a>
                <div class="stake_btn">
                    <div @click="stakePage = 'bsw'" class="btn" :class="{'active':stakePage=='bsw'}">
                      Stake BSW
                    </div>
                  <div @click="stakePage = 'tokens'" class="btn" :class="{'active':stakePage=='tokens'}">
                    Stake Tokens
                  </div>
                </div>
            </div>
            <div class="column cyberdex_stake">
                <div class="cyberdex">
                      <div class="d_flex">
                          <span>Use CyberDex <br>on mobile phone</span>
                          <p>Search for nft right in <br>your phone</p>
                        <a href="">
                          <div class="btn">
                            Let’s go!
                          </div>
                        </a>
                      </div>
                  <img src="/images/NFT3.png" alt="">
                </div>
            </div>
          </div>
      </div>
      <div class="bg_w">
        <div class="coins container">
          <div class="menu">
              <div class="links">
                <span @click="typeActive = 'active'" :class="{active:typeActive == 'active'}">Active</span>
                <span @click="typeActive = 'inactive'" :class="{active:typeActive == 'inactive'}">Inactive</span>
              </div>
              <div class="staked">
                <div @click="staked = !staked" class="btn" :class="{'stake-ellipse-true':staked}">
                  <img class="stake-ellipse" src="/images/stake-ellipse.png" alt="">
                  <img class="stake-row" src="/images/stake-row.png" alt="">
                </div>
                <span>Staked only</span>
              </div>
            <div class="search">
              <div class="input_wrap">
                <SvgImport name="search-normal"/>
                <input type="text" placeholder="Search farms">
              </div>
              <div class="select_wrap">
                <div @click="selectActive = !selectActive" class="click" >
                  <span>{{ selectData }}</span>
                  <SvgImport name="Down"/>
                </div>
                <div class="hidden" :class="{'hide':selectActive==false}">
                  <span @click="selectData='All'">All</span>
                  <span @click="selectData='Liquidity'">Liquidity</span>
                  <span @click="selectData='Apr'" >Apr</span>
                  <span @click="selectData='Stable'" >Stable</span>
                </div>
              </div>
            </div>
          </div>
          <div class="launch_wrap">
              <div class="item">
                <div class="row">
                    <div class="imgs">
                      <img class="full" src="/images/bsw-full.png" alt="">
                      <img class="small" src="/images/bsw-green.png" alt="">
                    </div>
                    <div class="column">
                        <div class="d_flex">
                          <span>Holder Pool</span>
                          <Helper typeImg="1" nameImg="farms-help.png" />
                        </div>
                        <p>Stake BSW - Ern BSW</p>
                        <span>+ participate in exclusive offers</span>
                      <h6> <c> APY </c>  69.96%</h6>
                    </div>
                </div>
                <div class="btn_unlock">
                  <SvgImport name="card-tick"/>
                   <span>Unlock Wallet</span>
                </div>
                <div class="details">
                    <span>Details</span>
                  <img src="/images/down.png" alt="">
                </div>
              </div>
              <div class="item">
              <div class="row">
                <div class="imgs">
                  <img class="full" src="/images/bsw-full.png" alt="">
                  <img class="small" src="/images/reload.png" alt="">
                </div>
                <div class="column">
                  <div class="d_flex">
                    <span>Auto Compound</span>
                    <Helper typeImg="1" nameImg="farms-help.png" />
                  </div>
                  <p class="mt">Stake BSW - Ern BSW</p>
                  <h6> <c> APY </c>  69.96%</h6>
                </div>
              </div>
              <div @click="showModalWallet" class="btn_unlock">
                <SvgImport name="card-tick"/>
                <span>Unlock Wallet</span>
              </div>
              <div class="details">
                <span>Details</span>
                <img src="/images/down.png" alt="">
              </div>
            </div>
              <div class="item">
              <div class="row">
                <div class="imgs">
                  <img class="full" src="/images/bsw-full.png" alt="">
                  <img class="small" src="/images/bsw-green.png" alt="">
                </div>
                <div class="column">
                  <div class="d_flex">
                    <span>Earn BSW</span>
                    <Helper typeImg="1" nameImg="farms-help.png" />
                  </div>
                  <p class="mt">Stake BSW</p>
                  <h6> <c> APY </c>  53.03%</h6>
                </div>
              </div>
              <div @click="showModalWallet" class="btn_unlock">
                <SvgImport name="card-tick"/>
                <span>Unlock Wallet</span>
              </div>
              <div class="details">
                <span>Details</span>
                <img src="/images/down.png" alt="">
              </div>
            </div>
            <div class="item">
              <div class="max">
                <span>max <br> 500</span>
              </div>
              <div class="row">
                <div class="imgs">
                  <img class="full" src="/images/eth 3.png" alt="">
                  <img class="small" src="/icons/bsw-full.png" alt="">
                </div>
                <div class="column">
                  <div class="d_flex">
                    <span>Earn ETH</span>
                    <img src="/images/farms-help.png" alt="">
                  </div>
                  <p>Stake BSW - Ern BSW</p>
                  <div class="w">
                      <div class="req">
                        Requirments
                      </div>
                    <img src="/images/farms-help.png" alt="">
                      <div class="hp">
                        200 BSW in HP
                      </div>
                  </div>
                  <h6> <c> APR </c>  80.15%</h6>
                </div>
              </div>
              <div @click="showModalWallet" class="btn_unlock">
                <SvgImport name="card-tick"/>
                <span>Unlock Wallet</span>
              </div>
              <div class="details">
                <span>Details</span>
                <img src="/images/down.png" alt="">
              </div>
            </div>
            <div class="item">
              <div class="max">
                <span>max <br> 500</span>
              </div>
              <div class="row">
                <div class="imgs">
                  <img class="full" src="/images/bnb.png" alt="">
                  <img class="small" src="/icons/bsw-full.png" alt="">
                </div>
                <div class="column">
                  <div class="d_flex">
                    <span>Earn WBNB</span>
                    <Helper typeImg="1" nameImg="farms-help.png" />
                  </div>
                  <p>Stake BSW - Ern BSW</p>
                  <div class="w">
                    <div class="req">
                      Requirments
                    </div>
                    <Helper typeImg="1" nameImg="farms-help.png" />
                    <div class="hp">
                      200 BSW in HP
                    </div>
                  </div>
                  <h6> <c> APR </c>  69.65%</h6>
                </div>
              </div>
              <div @click="showModalWallet" class="btn_unlock">
                <SvgImport name="card-tick"/>
                <span>Unlock Wallet</span>
              </div>
              <div class="details">
                <span>Details</span>
                <img src="/images/down.png" alt="">
              </div>
            </div>
            <div class="item">
              <div class="max">
                <span>max <br> 500</span>
              </div>
              <div class="row">
                <div class="imgs">
                  <img class="full" src="/images/bnb.png" alt="">
                  <img class="small" src="/icons/bsw-full.png" alt="">
                </div>
                <div class="column">
                  <div class="d_flex">
                    <span>Earn BTCB</span>
                    <Helper typeImg="1" nameImg="farms-help.png" />
                  </div>
                  <p>Stake BSW - Ern BSW</p>
                  <div class="w">
                    <div class="req">
                      Requirments
                    </div>
                    <Helper typeImg="1" nameImg="farms-help.png" />
                    <div class="hp">
                      200 BSW in HP
                    </div>
                  </div>
                  <h6> <c> APR </c>  76.73%</h6>
                </div>
              </div>
              <div @click="showModalWallet" class="btn_unlock">
                <SvgImport name="card-tick"/>
                <span>Unlock Wallet</span>
              </div>
              <div class="details">
                <span>Details</span>
                <img src="/images/down.png" alt="">
              </div>
            </div>
            <div class="item">
              <div class="row">
                <div class="imgs">
                  <img class="full" src="/images/bmvl 1.png" alt="">
                  <img class="small" src="/icons/bsw-full.png" alt="">
                </div>
                <div class="column">
                  <div class="d_flex">
                    <span>Earn bMVL</span>
                    <Helper typeImg="1" nameImg="farms-help.png" />
                  </div>
                  <p class="mt">Stake BSW - Ern BSW</p>
                  <h6> <c> APY </c>  84.81%</h6>
                </div>
              </div>
              <div @click="showModalWallet" class="btn_unlock">
                <SvgImport name="card-tick"/>
                <span>Unlock Wallet</span>
              </div>
              <div class="details">
                <span>Details</span>
                <img src="/images/down.png" alt="">
              </div>
            </div>
            <div class="item">
              <div class="row">
                <div class="imgs">
                  <img class="full" src="/images/gq 2.png" alt="">
                  <img class="small" src="/icons/bsw-full.png" alt="">
                </div>
                <div class="column">
                  <div class="d_flex">
                    <span>Earn GQ</span>
                    <Helper typeImg="1" nameImg="farms-help.png" />
                  </div>
                  <p class="mt">Stake BSW - Ern BSW</p>
                  <h6> <c> APY </c>  81.09%</h6>
                </div>
              </div>
              <div @click="showModalWallet" class="btn_unlock">
                <SvgImport name="card-tick"/>
                <span>Unlock Wallet</span>
              </div>
              <div class="details">
                <span>Details</span>
                <img src="/images/down.png" alt="">
              </div>
            </div>
            <div class="item">
              <div class="row">
                <div class="imgs">
                  <img class="full" src="/images/loa 1.png" alt="">
                  <img class="small" src="/icons/bsw-full.png" alt="">
                </div>
                <div class="column">
                  <div class="d_flex">
                    <span>Earn LOA</span>
                    <Helper typeImg="1" nameImg="farms-help.png" />
                  </div>
                  <p class="mt">Stake BSW - Ern BSW</p>
                  <h6> <c> APY </c>  40.40%</h6>
                </div>
              </div>
              <div @click="showModalWallet" class="btn_unlock">
                <SvgImport name="card-tick"/>
                <span>Unlock Wallet</span>
              </div>
              <div class="details">
                <span>Details</span>
                <img src="/images/down.png" alt="">
              </div>
            </div>
          </div>
      </div>
         <div class="launch">
           <div class="bg-green"></div>
           <div class="bg-red"></div>
           <div class="container">
              <div class="texts">
                <h2>Launch Your Project on Biswap <br>Now!</h2>
                <span>Farms stimulate users to provide liquidity for your trading pair by distributing BSW tokens to your pair’s LP token holders. Launchpool is a platform where a project owner can distribute tokens to BNB users who stake BSW tokens in the pool. When a project applies for Biswap Launchpool we can also create a new farming pair (subject to discussion) </span>
                <span>Biswap Launchpool and Farms are platforms that help project teams promote their token and get exposure to thousands of active Biswap users across the globe. We look for strong teams with clear and innovative vision in the crypto space. If you think you are one of the projects, do not wait any longer and apply below.</span>
                <div class="btn">
                  <SvgImport name="tick-circle"/>
                  <p>Apply to Launch</p>
                </div>
              </div>
             <img src="/images/launch-img.png" alt="">
           </div>
         </div>
        <div class="why">
            <div class="container">
                <div class="title">
                  Why choose us?
                </div>
               <div class="why_w">
                  <div class="wrap">
                    <img src="/images/why1.png" alt="">
                    <h3>Global Exposure</h3>
                    <span>Get access to 380k+ Biswap users <br>across the globe.</span>
                  </div>
                  <div class="wrap">
                    <img src="/images/why2.png" alt="">
                    <h3>Liquidity</h3>
                    <span>Projects launched on Biswap <br>Launchpool will be listed and have high <br>trading liquidity.</span>
                  </div>
                <div class="wrap">
                  <img src="/images/why3.png" alt="">
                  <h3>Token Distribution</h3>
                  <span>Projects launched on Biswap <br>Launchpool will be listed and have high <br>trading liquidity.</span>
                </div>
                <div class="wrap">
                  <img src="/images/why4.png" alt="">
                  <h3>Trading Competition</h3>
                  <span>Biswap will organize a tournament <br>dedicated to your project to maximize <br>trading volume with your token.</span>
                </div>
                <div class="wrap">
                  <img src="/images/why5.png" alt="">
                  <h3>Marketing Boost</h3>
                  <span>Your project will be promoted across all <br>our social media platforms with an <br>audience of over 320K+.</span>
                </div>
                <div class="wrap">
                  <img src="/images/why6.png" alt="">
                  <h3>Marketing Boost</h3>
                  <span>Your token might also be added to <br>Biswap Farms with high APR.</span>
                </div>
              </div>
            </div>
        </div>
      </div>
  </div>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport'
import Exchange from '~/components/Exchange'
import Helper from '~/components/Helper';
export default {
  mounted() {
    this.$nuxt.$emit('active-page', 5);
  },
  methods: {
    showModalWallet(){
      this.$nuxt.$emit('showModalConnectWallet');
    }
  },
  data: function () {
    return {
      stakePage:"bsw",
      typeActive:'active',
      staked:false,
      selectActive: false,
      selectData: 'All',
    }
  },
  components:{
    SvgImport,
    Exchange,
    Helper,
  }
}
</script>
