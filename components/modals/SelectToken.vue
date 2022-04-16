<template>
  <div v-if="modalCurrency" class="select_token">
    <div class="title">
      <span>Add Liquidity</span>
      <div class="close" @click="modalCurrency = false">
        <img src="/images/close.png" alt="">
      </div>
    </div>
    <div class="search">
      <input type="text" placeholder="Search name or paste adress">
    </div>
    <div class="common_bases">
      <div class="head">
        <span>Common bases</span>
        <Helper typeImg="1" nameImg="modal-help.png" />
      </div>
      <div class="wrap">
        <div @click="getCrypto(1,index)" v-for="(crypto, index) in commonBases" :key="index"  class="row">
          <img :src="'/images/coins/' + crypto.img" alt="">
          <span>{{crypto.name}}</span>
        </div>
      </div>
    </div>
    <div class="content">
      <div class="head">
        <span>Token Name</span>
        <div class="sort">
          <img src="/images/sort.png" alt="">
        </div>
      </div>
      <div class="wrap">
        <div class="coins">
          <div v-for="(crypto, index) in tokensMain" :key="index" class="row">
            <img :src="'/images/coins/' + crypto.img" alt="">
            <span>{{crypto.name}}</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport';
import Helper from '~/components/Helper';
export default {
  props: {

  },
  data: function () {
    return {
      selectCoin:false,
      modalCurrency:false,
      exchangeNumber:null,
      commonBases:[
        {
          name: 'BSW',
          img: 'bsw.svg',
          count: null,
          usdPricePerOne: 1.05,
          tradeFee: 0.01,
          usdPriceAll: null,
        },
        {
          name: 'BUSD',
          img: 'busd.svg',
          count: null,
          usdPricePerOne: 1.05,
          tradeFee: 0.01,
          usdPriceAll: null,
        },
        {
          name: 'USDT',
          img: 'usdt.svg',
          count: null,
          usdPricePerOne: 1.05,
          tradeFee: 0.01,
          usdPriceAll: null,
        },
        {
          name: 'USDC',
          img: 'usdc.svg',
          count: null,
          usdPricePerOne: 1.05,
          tradeFee: 0.01,
          usdPriceAll: null,
        },
        {
          name: 'BTCB',
          img: 'btcb.svg',
          count: null,
          usdPricePerOne: 1.05,
          tradeFee: 0.01,
          usdPriceAll: null,
        },
        {
          name: 'ETH',
          img: 'eth.svg',
          count: null,
          usdPricePerOne: 2.05,
          tradeFee: 0.01,
          usdPriceAll: null,
        },
        {
          name: 'BSW',
          img: 'bsw.svg',
          count: null,
          usdPricePerOne: 1.05,
          tradeFee: 0.01,
          usdPriceAll: null,
        },
        {
          name: 'BFG',
          img: 'bfg.svg',
          count: null,
          usdPricePerOne: 1.05,
          tradeFee: 0.01,
          usdPriceAll: null,
        }
      ],
      tokensMain:[
        {
          name: 'BNB',
          img: 'bnb.svg',
          count: null,
          usdPricePerOne: 1.05,
          tradeFee: 0.01,
          usdPriceAll: null,
        },
        {
          name: 'ADA',
          img: 'ada.svg',
          count: null,
          usdPricePerOne: 1.05,
          tradeFee: 0.01,
          usdPriceAll: null,
        },
        {
          name: 'AIRT',
          img: 'airt.svg',
          count: null,
          usdPricePerOne: 1.05,
          tradeFee: 0.01,
          usdPriceAll: null,
        },
        {
          name: 'ALPACA',
          img: 'alpaca.svg',
          count: null,
          usdPricePerOne: 1.05,
          tradeFee: 0.01,
          usdPriceAll: null,
        },        {
          name: 'BNB',
          img: 'bnb.svg',
          count: null,
          usdPricePerOne: 1.05,
          tradeFee: 0.01,
          usdPriceAll: null,
        },
        {
          name: 'ADA',
          img: 'ada.svg',
          count: null,
          usdPricePerOne: 1.05,
          tradeFee: 0.01,
          usdPriceAll: null,
        },
        {
          name: 'AIRT',
          img: 'airt.svg',
          count: null,
          usdPricePerOne: 1.05,
          tradeFee: 0.01,
          usdPriceAll: null,
        },
        {
          name: 'ALPACA',
          img: 'alpaca.svg',
          count: null,
          usdPricePerOne: 1.05,
          tradeFee: 0.01,
          usdPriceAll: null,
        },
      ]
    }
  },
  methods: {
    getCrypto(type,index){
        if (type == 1)
        {
          this.selectCoin = this.commonBases[index];

        }
        else if (type == 2)
        {
          this.selectCoin = this.selectCoin[index];
        }
        this.selectCoin.exchangeNumber = this.exchangeNumber;
        this.modalCurrency=false;
        this.$emit('getCrypto', {
            selectCoin:this.selectCoin
        })
    }
  },
  name: "SelectToken",
  components: {
    SvgImport,
    Helper,
  }
}


</script>

