<template>
  <div class="refferal">
      <div class="main">
          <div class="bg-ellipse-red"></div>
          <div class="bg-ellipse-green"></div>
          <div class="container">
            <div class="column">
                <h1>Invite your friends. <br> Earn cryptocurrency together</h1>
                <h2>
                  Earn up to 20% from friends’ swap commission on Biswap <br>and 5% from their earnings on Farms & Launchpools                </h2>
              <a href="">
              <div class="add_ref">
                  <img src="/images/people.svg" alt="">
                  <span>Invite friends</span>
                </div>
              </a>
            </div>
          </div>
        <img class="ido_img pc" src="/images/refferal-img.png" alt="">
        <img class="ido_img tablet" src="/images/referral-bg-mob.png" alt="">
        <img class="ido_img mob" src="/images/referral-bg-mob2.png" alt="">
      </div>
      <div class="bg_w">
        <div class="container">
          <div class="how_to">
              <div class="title_wrap">
                <h2>How to invite friends?</h2>
                <div class="investor">
                  <img src="/images/ido-what.svg" alt="">
                  <span>my inviter:</span>
                  <p>78asd...dfiud</p>
                  <div>
                    10%
                  </div>
                </div>
              </div>
            <div class="wrap">
              <div class="item">
                  <div class="count count1">
                    1
                  </div>
                <img src="/images/ref-img-1.png" alt="">
                <h4>Get a referral link</h4>
                <span>Connect a wallet and generate your <br>referral link in the Referral section.</span>
              </div>
              <div class="item">
                <div class="count count2">
                  2
                </div>
                <img src="/images/ref-img-2.png" alt="">
                <h4>Invite friends</h4>
                <span>Invite your friends to register <br>via your referral link</span>
              </div>
              <div class="item">
                <div class="count count3">
                  3
                </div>
                <img src="/images/ref-img-3.png" alt="">
                <h4>Earn crypto</h4>
                <span>Receive referral rewards in BSW tokens <br>from your friends’ earnings & swaps</span>
              </div>
              <div class="text_item">
                 <h5>Farms Referral Rewards</h5>
                  <span>Gain 5% from your friends earnings on Farms! Your rewards will be displayed on the referral balance at the moment your invited friends withdraw their earned BSW tokens.</span>
                <a href="">Read more</a>
              </div>
              <div class="text_item">
                <h5>Launchpools Referral Rewards</h5>
                <span>
                    Get 5% of from friends’ profit obtained in Launchpools! The reward is only valid for the pool in which BSW is staked in return for more BSW.
                </span>
                  <a href="">Read more</a>
              </div>
              <div class="text_item">
                <h5>Launchpools Referral Rewards</h5>
                <span>
                  Get up to 20% from friends’ swap commission each time your friend makes a swap! Receive your reward immediately after the swap is made. Swaps referral program will be active for certain pairs only.                </span>
                <a href="">Read more</a>
              </div>
            </div>
          </div>
          <div class="faq">
              <h2>
                FAQ
              </h2>
            <ul class="lists">
              <li  v-for="(faq, index) in faqItems" :key="index" class="item_wrap" :class="{'column-break':index == 6}" >
                <div @click="showItem(index)" class="item">
                  <span>{{faq.question}}</span>
                  <img :class="{'active':statusShowItem[index]}" src="/images/down.svg" alt="">
                </div>
                <div class="item_hidden" :class="{'active':statusShowItem[index]}">
                  {{faq.answer}}
                </div>
              </li>
            </ul>
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
  data: function () {
    return {

      statusShowItem: {},
      faqItems: [
        {
          question: 'Where do I get my referral link?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'How much crypto can I earn via the Swap Referral Program?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'How do I invite a referral friend?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'Is the Swap referral program active for all swap pairs?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'Are there separate balances for referral rewards from friends\' Swaps, Farms, Launchpools?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'What percentage of Swap referral rewards will I earn if I have 0 BSW staked in BSW Holder Pool?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'How do I generate a new referral link?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'How much can I earn from my friends\' Farms & Launchpools?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'How does profit sharing work?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'Is Referral Program Active for all Launchpools?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'Where are all my generated referral links?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'When will I get my referral reward from Farms & Launchpools?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'In what crypto currency the referral commission is accounted to my referral balance?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'Can I profit from the Referral Program without any investments from my side?',
          answer: 'Answer text duration of XPS IDO on Biswap Launchpad'
        },
        {
          question: 'Are there fees for referral rewards withdrawal from referral balances?',
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
  mounted() {
    this.$nuxt.$emit('active-page', 7);
  },
  components:{
    SvgImport,
    Exchange,
  }
}
</script>
