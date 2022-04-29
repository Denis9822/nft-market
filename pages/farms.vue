<template>
  <div class="farms">
      <div class="main">
          <div class="bg-ellipse-red"></div>
          <div class="bg-ellipse-green"></div>
          <div class="container">
            <div class="column">
              <div class="wr">
                <h1>Farms</h1>
                <div @click="detailFarms = !detailFarms" class="details mob">
                    <span>Details</span>
                  <div class="" :class="{'hidden-mob':detailFarms == true}">
                  <SvgImport name="details-arrow-up"/>
                  </div>
                  <div class="" :class="{'hidden-mob':detailFarms == false}" >
                  <SvgImport name="details-arrow-down"/>
                  </div>
                </div>
              </div>
              <div class="block" :class="{'hidden-mob':detailFarms == true}" >
                <h2>
                  Biswap Farms offer multiple farming opportunities to you. <br>Get double rewards by staking your LP tokens in return for
                  <br>additional BSW tokens and earning high income from <br>swap transactions
                </h2>
              <a href="">
                <div class="add">
                  <span>Add project</span>
                  <img src="/images/plus.svg" alt="">
                </div>
              </a>
              </div>
            </div>
            <div class="column" :class="{'hidden-mob':detailFarms == true}">
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
                <span @click="typeActive = 'live'" :class="{active:typeActive == 'live'}">Live</span>
                <span @click="typeActive = 'main'" :class="{active:typeActive == 'main'}">Main</span>
                <span @click="typeActive = 'innovation'" :class="{active:typeActive == 'innovation'}">Innovation</span>
                <span @click="typeActive = 'gamefi'" :class="{active:typeActive == 'gamefi'}">GameFi</span>
                <span @click="typeActive = 'archive'" :class="{active:typeActive == 'archive'}">Archive</span>
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
                  <div class="btn">
                    Harvest All
                  </div>
              </div>
          </div>

          <div class="coin_wrap">
            <div class="row after">
                  <div class="status red">
                    Hot
                  </div>
                  <div class="coins">
                      <div class="imgs">
                        <img src="/images/coins/usdt.svg" alt="">
                        <img src="/images/coins/bsw.svg" alt="">
                      </div>
                      <div class="name">
                          USDT-BSW
                      </div>
                  </div>
                  <div class="apy">
                      <p>APY</p>
                      <div class="d_flex">
                        <span>219.46%</span>
                        <Helper typeImg="1" nameImg="farms-help.png" />
                      </div>
                  </div>
                  <div class="apr">
                    <div class="d_flex d_flex1">
                      <p>APR</p>
                      <Helper typeImg="1" nameImg="farms-help.png" />
                    </div>
                    <div class="d_flex">
                      <span>219.46%</span>
                      <img src="/images/farms-computing.png" alt="">
                    </div>
                  </div>
                  <div class="liq">
                    <p>Liquidity</p>
                    <div class="d_flex">
                      <span>219.46%</span>
                      <Helper typeImg="1" nameImg="farms-help.png" />
                    </div>
                  </div>
                  <div class="earn">
                      <p>Earned</p>
                      <span>-</span>
                  </div>
                      <div @click="detailsRow = !detailsRow" class="details">
                      <span>Details</span>
                      <img src="/images/down.png" alt="">
                  </div>
                  <div class="warning">
                    <DetailsHelper typeImg="1" nameImg="farms-warning.png" />
                  </div>
              </div>
            <div v-if="detailsRow" class="row mob row_hidden_mob">
              <div class="apr2">
                <h4>APR</h4>
              </div>
              <div class="btn_next">
                  <span>219.46%</span>
                  <img src="/images/farms-computing.png" alt="">
              </div>
              <div class="liquidity">
                <h4>Liquidity</h4>
              </div>
              <div class="liquidity_d_flex">
                <span>$15 479 471</span>
                <Helper typeImg="1" nameImg="farms-help.png" />
              </div>
            </div>
            <div v-if="detailsRow" class="row row_hidden">
              <div class="getlp">
                Get LP
              </div>
               <div class="available">
                 <h4>Available LP</h4>
                 <span>0 LP</span>
                 <p>$0.0000</p>
               </div>
                <div class="btn_next">
                  <img src="/images/next.png" alt="">
                </div>
                <div @click="showModalWallet" class="btn_wallet">
                  <SvgImport name="card-tick"/>
                  <span>Unlock Wallet</span>
                </div>
              <div class="btn_next">
                <img src="/images/next.png" alt="">
              </div>
              <div class="btn_harvest">
                Harvest
              </div>
              <div class="earned">
                <h4>Earned</h4>
                <span>0 BSW</span>
                <p>$0.0000</p>
              </div>
            </div>
            <div class="row after">
              <div class="status red">
                Hot
              </div>
              <div class="coins">
                <div class="imgs">
                  <img src="/images/coins/usdt.svg" alt="">
                  <img src="/images/coins/bsw.svg" alt="">
                </div>
                <div class="name">
                  USDT-BSW
                </div>
              </div>
              <div class="apy">
                <p>APY</p>
                <div class="d_flex">
                  <span>219.46%</span>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
              </div>
              <div class="apr">
                <div class="d_flex d_flex1">
                  <p>APR</p>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
                <div class="d_flex">
                  <span>219.46%</span>
                  <img src="/images/farms-computing.png" alt="">
                </div>
              </div>
              <div class="liq">
                <p>Liquidity</p>
                <div class="d_flex">
                  <span>219.46%</span>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
              </div>
              <div class="earn">
                <p>Earned</p>
                <span>-</span>
              </div>
              <div @click="detailsRow = !detailsRow" class="details">
                <span>Details</span>
                <img src="/images/down.png" alt="">
              </div>
              <div class="warning">
                <DetailsHelper typeImg="1" nameImg="farms-warning.png" />
              </div>
            </div>
            <div class="row after">
              <div class="status red">
                Hot
              </div>
              <div class="coins">
                <div class="imgs">
                  <img src="/images/coins/usdt.svg" alt="">
                  <img src="/images/coins/bsw.svg" alt="">
                </div>
                <div class="name">
                  USDT-BSW
                </div>
              </div>
              <div class="apy">
                <p>APY</p>
                <div class="d_flex">
                  <span>219.46%</span>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
              </div>
              <div class="apr">
                <div class="d_flex d_flex1">
                  <p>APR</p>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
                <div class="d_flex">
                  <span>219.46%</span>
                  <img src="/images/farms-computing.png" alt="">
                </div>
              </div>
              <div class="liq">
                <p>Liquidity</p>
                <div class="d_flex">
                  <span>219.46%</span>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
              </div>
              <div class="earn">
                <p>Earned</p>
                <span>-</span>
              </div>
              <div @click="detailsRow = !detailsRow" class="details">
                <span>Details</span>
                <img src="/images/down.png" alt="">
              </div>
              <div class="warning">
                <DetailsHelper typeImg="1" nameImg="farms-warning.png" />
              </div>
            </div>
            <div class="row after">
              <div class="status green">
                New
              </div>
              <div class="coins">
                <div class="imgs">
                  <img src="/images/coins/usdt.svg" alt="">
                  <img src="/images/coins/bsw.svg" alt="">
                </div>
                <div class="name">
                  USDT-BSW
                </div>
              </div>
              <div class="apy">
                <p>APY</p>
                <div class="d_flex">
                  <span>219.46%</span>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
              </div>
              <div class="apr">
                <div class="d_flex d_flex1">
                  <p>APR</p>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
                <div class="d_flex">
                  <span>219.46%</span>
                  <img src="/images/farms-computing.png" alt="">
                </div>
              </div>
              <div class="liq">
                <p>Liquidity</p>
                <div class="d_flex">
                  <span>219.46%</span>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
              </div>
              <div class="earn">
                <p>Earned</p>
                <span>-</span>
              </div>
              <div @click="detailsRow = !detailsRow" class="details">
                <span>Details</span>
                <img src="/images/down.png" alt="">
              </div>
              <div class="warning">
                <DetailsHelper typeImg="1" nameImg="farms-warning.png" />
              </div>
            </div>
            <div class="row after">
              <div class="status blue">
                Boosted
              </div>
              <div class="coins">
                <div class="imgs">
                  <img src="/images/coins/usdt.svg" alt="">
                  <img src="/images/coins/bsw.svg" alt="">
                </div>
                <div class="name">
                  USDT-BSW
                </div>
              </div>
              <div class="apy">
                <p>APY</p>
                <div class="d_flex">
                  <span>219.46%</span>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
              </div>
              <div class="apr">
                <div class="d_flex d_flex1">
                  <p>APR</p>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
                <div class="d_flex">
                  <span>219.46%</span>
                  <img src="/images/farms-computing.png" alt="">
                </div>
              </div>
              <div class="liq">
                <p>Liquidity</p>
                <div class="d_flex">
                  <span>219.46%</span>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
              </div>
              <div class="earn">
                <p>Earned</p>
                <span>-</span>
              </div>
              <div @click="detailsRow = !detailsRow" class="details">
                <span>Details</span>
                <img src="/images/down.png" alt="">
              </div>
              <div class="warning">
                <DetailsHelper typeImg="1" nameImg="farms-warning.png" />
              </div>
            </div>
            <div class="row after">
              <div class="status blue">
                Boosted
              </div>
              <div class="coins">
                <div class="imgs">
                  <img src="/images/coins/usdt.svg" alt="">
                  <img src="/images/coins/bsw.svg" alt="">
                </div>
                <div class="name">
                  USDT-BSW
                </div>
              </div>
              <div class="apy">
                <p>APY</p>
                <div class="d_flex">
                  <span>219.46%</span>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
              </div>
              <div class="apr">
                <div class="d_flex d_flex1">
                  <p>APR</p>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
                <div class="d_flex">
                  <span>219.46%</span>
                  <img src="/images/farms-computing.png" alt="">
                </div>
              </div>
              <div class="liq">
                <p>Liquidity</p>
                <div class="d_flex">
                  <span>219.46%</span>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
              </div>
              <div class="earn">
                <p>Earned</p>
                <span>-</span>
              </div>
              <div @click="detailsRow = !detailsRow" class="details">
                <span>Details</span>
                <img src="/images/down.png" alt="">
              </div>
              <div class="warning">
                <DetailsHelper typeImg="1" nameImg="farms-warning.png" />
              </div>
            </div>
            <div class="row after">
              <div class="status blue">
                Boosted
              </div>
              <div class="coins">
                <div class="imgs">
                  <img src="/images/coins/usdt.svg" alt="">
                  <img src="/images/coins/bsw.svg" alt="">
                </div>
                <div class="name">
                  USDT-BSW
                </div>
              </div>
              <div class="apy">
                <p>APY</p>
                <div class="d_flex">
                  <span>219.46%</span>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
              </div>
              <div class="apr">
                <div class="d_flex d_flex1">
                  <p>APR</p>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
                <div class="d_flex">
                  <span>219.46%</span>
                  <img src="/images/farms-computing.png" alt="">
                </div>
              </div>
              <div class="liq">
                <p>Liquidity</p>
                <div class="d_flex">
                  <span>219.46%</span>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
              </div>
              <div class="earn">
                <p>Earned</p>
                <span>-</span>
              </div>
              <div @click="detailsRow = !detailsRow" class="details">
                <span>Details</span>
                <img src="/images/down.png" alt="">
              </div>
              <div class="warning">
                <DetailsHelper typeImg="1" nameImg="farms-warning.png" />
              </div>
            </div>
            <div class="row after">
              <div class="status blue">
                Boosted
              </div>
              <div class="coins">
                <div class="imgs">
                  <img src="/images/coins/usdt.svg" alt="">
                  <img src="/images/coins/bsw.svg" alt="">
                </div>
                <div class="name">
                  USDT-BSW
                </div>
              </div>
              <div class="apy">
                <p>APY</p>
                <div class="d_flex">
                  <span>219.46%</span>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
              </div>
              <div class="apr">
                <div class="d_flex d_flex1">
                  <p>APR</p>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
                <div class="d_flex">
                  <span>219.46%</span>
                  <img src="/images/farms-computing.png" alt="">
                </div>
              </div>
              <div class="liq">
                <p>Liquidity</p>
                <div class="d_flex">
                  <span>219.46%</span>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
              </div>
              <div class="earn">
                <p>Earned</p>
                <span>-</span>
              </div>
              <div @click="detailsRow = !detailsRow" class="details">
                <span>Details</span>
                <img src="/images/down.png" alt="">
              </div>
              <div class="warning">
                <DetailsHelper typeImg="1" nameImg="farms-warning.png" />
              </div>
            </div>
            <div class="row after">
              <div class="status blue">
                Boosted
              </div>
              <div class="coins">
                <div class="imgs">
                  <img src="/images/coins/usdt.svg" alt="">
                  <img src="/images/coins/bsw.svg" alt="">
                </div>
                <div class="name">
                  USDT-BSW
                </div>
              </div>
              <div class="apy">
                <p>APY</p>
                <div class="d_flex">
                  <span>219.46%</span>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
              </div>
              <div class="apr">
                <div class="d_flex d_flex1">
                  <p>APR</p>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
                <div class="d_flex">
                  <span>219.46%</span>
                  <img src="/images/farms-computing.png" alt="">
                </div>
              </div>
              <div class="liq">
                <p>Liquidity</p>
                <div class="d_flex">
                  <span>219.46%</span>
                  <Helper typeImg="1" nameImg="farms-help.png" />
                </div>
              </div>
              <div class="earn">
                <p>Earned</p>
                <span>-</span>
              </div>
              <div @click="detailsRow = !detailsRow" class="details">
                <span>Details</span>
                <img src="/images/down.png" alt="">
              </div>
              <div class="warning">
                <DetailsHelper typeImg="1" nameImg="farms-warning.png" />
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
                <a href="">
                <div class="btn">
                  <SvgImport name="tick-circle"/>
                  <p>Apply to Launch</p>
                </div>
                </a>
              </div>
             <img src="/images/launch-img.svg" alt="">
           </div>
         </div>
        <div class="why">
            <div class="container">
                <div class="title">
                  Why choose us?
                </div>
              <div class="slider mob">
                <div class="slider_wrap">
                  <carousel v-if="!loading" perPage="1" paginationEnabled="false" navigationEnabled="false">
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
      </div>
  </div>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport'
import Exchange from '~/components/Exchange'
import DetailsHelper from '~/components/farms/DetailsHelper'
import Helper from '~/components/Helper';
export default {
  mounted() {
    this.$nuxt.$emit('active-page', 4);
  },
  methods: {
    showModalWallet(){
      this.$nuxt.$emit('showModalConnectWallet');
    }
  },
  data: function () {
    return {
      typeActive:"live",
      staked:false,
      search:null,
      selectActive:false,
      selectData:'All',
      detailsRow:false,
      detailFarms:true,
    }
  },
  components:{
    SvgImport,
    Exchange,
    Helper,
    DetailsHelper,
  }
}
</script>
