<template>
  <div class="ido">
      <div class="main">
          <div class="bg-ellipse-red"></div>
          <div class="bg-ellipse-green"></div>
          <div class="container">
            <div class="column">
                <h1>IDO Launchpad</h1>
                <h2>
                  Buy new tokens directly for BSW on Biswap. Maximize your profit <br>by participating in the Initial DEX Offerings.
                </h2>
              <a href="">
                <div class="add">
                  <span>Launch your project</span>
                  <img src="/images/plus.png" alt="">
                </div>
              </a>
            </div>
          </div>
        <img class="ido_img" src="/images/ido-img.png" alt="">
      </div>
      <div class="bg_w">
        <div class="container">
          <div class="ido_lists">
            <div class="links">
              <span @click="typeActive = 'active'" :class="{active:typeActive == 'active'}">Active</span>
              <span @click="typeActive = 'inactive'" :class="{active:typeActive == 'inactive'}">Inactive</span>
            </div>
            <div class="list">
                <div class="about">
                    <div class="logo_status">
                      <img src="/images/xps-full.png" alt="">
                      <img src="/images/xps-logo.png" alt="">
                      <span>Ended</span>
                    </div>
                  <div class="desc">
                    Xpansion is a decentralized <br>4x strategy P2E game which will be <br>set in the nearest future.
                  </div>
                  <div class="social">
                    <a href="">
                      <img src="/images/telegram.png" alt="">
                    </a>
                    <a href="">
                      <img src="/images/twitter.png" alt="">
                    </a>
                    <a href="">
                      <img src="/images/m.png" alt="">
                    </a>
                  </div>
                  <div class="links">
                    <a href="">
                        <span>Website</span>
                        <img src="/images/link.png" alt="">
                    </a>
                    <a href="">
                      <span>Whitepaper</span>
                      <img src="/images/link.png" alt="">
                    </a>
                    <a href="">
                      <span>View Contract</span>
                      <img src="/images/link.png" alt="">
                    </a>
                  </div>
                </div>
                <div class="option">
                  <div class="top">
                      <div class="imgs">
                        <img class="big" src="/images/xps-full.png" alt="">
                        <img class="small" src="/images/bsw-full.png" alt="">
                      </div>
                      <div class="about">
                          <div class="row">
                              <span>Limited Option</span>
                              <img src="/images/ado-what.png" alt="">
                          </div>
                          <h3>Deposit BSW - Get XPS</h3>
                          <div class="btn">
                            <img src="/images/bsw-full.png" alt="">
                            <span>57.17 BSW</span>
                          </div>
                      </div>
                  </div>
                  <div class="bottom">
                    <div class="row">
                        <span>Funds to raise:</span>
                        <p>$300 000</p>
                    </div>
                    <div class="row">
                      <span>Token offered:</span>
                      <p>2 500 000 XPS</p>
                    </div>
                    <div class="row">
                      <span>Price per XPS</span>
                      <p>0.0686 BSW (~$0.12)</p>
                    </div>
                    <div class="row">
                      <span>BSW to burn</span>
                      <p>~$45 000</p>
                    </div>
                    <div class="row">
                      <span>Total raised</span>
                      <p>~$3 846 938</p>
                    </div>
                  </div>
                </div>
                <div class="option">
                  <div class="top">
                    <div class="imgs">
                      <img class="big" src="/images/xps-full.png" alt="">
                      <img class="small" src="/images/bsw-full.png" alt="">
                    </div>
                    <div class="about">
                      <div class="row">
                        <span>Limited Option</span>
                        <img src="/images/ado-what.png" alt="">
                      </div>
                      <h3>Deposit BSW - Get XPS</h3>
                      <div class="btn">
                        <img src="/images/bsw-full.png" alt="">
                        <span>Unlimited</span>
                      </div>
                    </div>
                  </div>
                  <div class="bottom">
                    <div class="row">
                      <span>Funds to raise:</span>
                      <p>$900 000</p>
                    </div>
                    <div class="row">
                      <span>Token offered:</span>
                      <p>7 500 000 XPS</p>
                    </div>
                    <div class="row">
                      <span>Price per XPS</span>
                      <p>0.0686 BSW (~$0.12)</p>
                    </div>
                    <div class="row">
                      <span>BSW to burn</span>
                      <p>~$135 000</p>
                    </div>
                    <div class="row">
                      <span>Total raised</span>
                      <p>~$46 240 275</p>
                    </div>
                  </div>
                </div>
            </div>

          </div>
          <div class="how_to">
              <h2>How to participate in IDO Launchpad?</h2>
            <div class="wrap">
              <div class="item">
                  <div class="count count1">
                    1
                  </div>
                <img src="/images/how-to-1.png" alt="">
                <h4>Prepare BSW</h4>
                <span>Prepare BSW in your wallet before the <br>IDO Launchpad starts on Biswap.</span>
              </div>
              <div class="item">
                <div class="count count2">
                  2
                </div>
                <img src="/images/how-to-2.png" alt="">
                <h4>Buy Tokens</h4>
                <span>Deposit your BSW to buy tokens <br>within the tokens' sale duration.</span>
              </div>
              <div class="item">
                <div class="count count3">
                  3
                </div>
                <img src="/images/how-to-3.png" alt="">
                <h4>Collect your tokens</h4>
                <span>Withdraw your purchased tokens <br>under proportion after the closure of <br>IDO for Biswap Launchpad.</span>
              </div>

            </div>
          </div>
          <div class="faq">
              <h2>
                FAQ
              </h2>
              <ul class="lists">
                <li  v-for="(faq, index) in faqItems" :key="index" class="item_wrap" :class="{'column-break':index == 3}" >
                  <div @click="showItem(index)" class="item">
                      <span>{{faq.question}}</span>
                      <img :class="{'active':statusShowItem[index]}" src="/images/down.png" alt="">
                  </div>
                  <div class="item_hidden" :class="{'active':statusShowItem[index]}">
                    {{faq.answer}}
                  </div>
                </li>
              </ul>
          </div>
          <div class="apply_project">
            <div class="bg-1"></div>
            <div class="bg-2"></div>
            <div class="img">
              <img src="/images/apply-project.png" alt="">
            </div>
            <div class="column">
              <h2>Want to launch your project <br> on Biswap IDO Launchpad?</h2>
              <h3>Launch your project on Biswap to introduce it to the most fast-growing <br>and active community on BNB CHAIN.</h3>
              <a href="">
              <div class="btn">
                Apply to launch
              </div>
              </a>
            </div>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport'
import Exchange from '~/components/Exchange'
export default {
  mounted() {
    this.$nuxt.$emit('active-page', 6);
  },
  data: function () {
    return {
      typeActive: 'active',
      statusShowItem: {},
      faqItems: [
        {
          question: 'What\'s duration of XPS IDO on Biswap Launchpad?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'Is there any fee to participate?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'What\'s the difference between limited and unlimited deposit options for participation?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'Can I participate in both the limited and unlimited deposit options at the same time?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'How are tokens distributed on the launchpad, depending on the amount of funds collected?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'When can I withdraw gained tokens on Biswap Launchpad?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'How are tokens distributed on the launchpad, depending on the amount of funds collected?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
      ],
    }
  },
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
    Exchange,
  }
}
</script>
