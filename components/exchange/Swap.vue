<template>
  <div v-if="pageActive==1" class="swap">
    <div class="texts">
      <div class="column">
        <h4>Exchange</h4>
        <span>Trade tokens in an instant</span>
      </div>
      <SvgImport name="setting-2"/>
    </div>
    <div class="form_w">
      <div class="sw" :class="{flex_reverse:swapStatus}">
        <div class="input_w">
          <div v-if="typeFrom == 2" class="txt">
            From (estimated)
          </div>
          <div class="w">
            <input v-model="exchangeFrom.count" @input="setData(1)" type="number" placeholder="0.0">
            <div @click="showModalCurrency(1)" class="coin_select">
              <img :src="'/images/coins/' + exchangeFrom.img" alt="">
              <span>{{ exchangeFrom.name }}</span>
              <img src="/images/down.png" alt="">
            </div>
          </div>
          <div v-if="exchangeFrom.count > 0 || exchangeTo.count > 0" class="price_w">
            <div class="price">~${{ exchangeResult.countUsd }}</div>
            <div class="currency">{{ exchangeFrom.name }}</div>
          </div>
        </div>
        <div @click="swap()" class="change">
          <img src="/images/Swipe.svg" alt="">
        </div>
        <div class="input_w">
          <div v-if="typeFrom == 1" class="txt">
            To (estimated)
          </div>
          <div class="w">
            <input v-model="exchangeTo.count" @input="setData(2)" type="number" placeholder="0.0">
            <div @click="showModalCurrency(2)" class="coin_select">
              <img :src="'/images/coins/' + exchangeTo.img" alt="">
              <span>{{ exchangeTo.name }}</span>
              <img src="/images/down.png" alt="">
            </div>
          </div>
          <div v-if="exchangeFrom.count > 0 || exchangeTo.count > 0" class="price_w">
            <div class="price">~${{ exchangeResult.countUsd }}</div>
            <div class="currency">{{ exchangeTo.name }}</div>
          </div>
        </div>
      </div>
      <div v-if="exchangeFrom.count > 0 || exchangeTo.count > 0" class="price_change">
        <div class="left">
          Price
        </div>
        <div class="right">
          <span >{{parseFloat(coinInfo().price).toFixed(5)}} {{coinInfo().name1}} per {{coinInfo().name2}}</span>
          <img @click="swapPricePerCoins = !swapPricePerCoins" src="/images/unlock.png" alt="">
        </div>
      </div>

      <div @click="showModalWallet" class="btn">
        <SvgImport name="card-tick"/>
        <span>Unlock Wallet</span>
      </div>
      <div v-if="exchangeFrom.count > 0 || exchangeTo.count > 0" class="trade_info">
        <div class="row">
          <span>Minimum received</span>
          <p>64890 {{coinInfo().name2}}</p>
        </div>
        <div class="row">
          <span>Price Impact</span>
          <h4>0.52%</h4>
        </div>
        <div class="row">
          <span>Trade fee</span>
          <p>0.1 {{coinInfo().name1}} ~ 41.1612 $</p>
        </div>
      </div>
    </div>
    <SelectToken @getCrypto='onGetCrypto' ref="modal"/>
  </div>
</template>

<script>
import SvgImport from '~/components/layout/SvgImport';
import Helper from '~/components/Helper';
import SelectToken from '~/components/modals/SelectToken';
export default {
  props: {
    pageActive: {type: String, default: 0},
  },
  data: function () {
    return {
      modalClose: false,
      typeFrom: null,
      swapStatus: false,
      modalCurrency: false,
      swapPricePerCoins:false,
      exchangeFrom: {
        name: 'BNB',
        img: 'bnb.svg',
        count: null,
        usdPricePerOne: 420.5,
        tradeFee: 0.01,
        usdPriceAll: null,
      },
      exchangeTo: {
        name: 'BSW',
        img: 'bsw.svg',
        count: null,
        usdPricePerOne: 1.05,
        tradeFee: 0.01,
        usdPriceAll: null,
      },
      exchangeResult: {
        countUsd: null,
      }
    }
  },
  methods: {
    coinInfo(){
      let name1 = null;
      let name2 = null;
      let price = null;
        if (this.typeFrom == 1 || this.swapPricePerCoins==false)
        {
            name1 = this.exchangeFrom.name;
            name2 =this.exchangeTo.name;
            price = this.exchangeTo.usdPricePerOne/this.exchangeFrom.usdPricePerOne;
        }
        if (this.typeFrom == 2 || this.swapPricePerCoins==true ){
          name1 = this.exchangeTo.name;
          name2 =this.exchangeFrom.name;
          price = this.exchangeFrom.usdPricePerOne/this.exchangeTo.usdPricePerOne;
        }
        return {name1: name1, name2: name2, price: price};
    },
    onGetCrypto(data){
      let data1 = data.selectCoin;
      if (data1.exchangeNumber == 1) {
        this.exchangeFrom.name = data1.name;
        this.exchangeFrom.img = data1.img;
        this.exchangeFrom.usdPricePerOne = data1.usdPricePerOne;
        this.exchangeFrom.tradeFee = data1.tradeFee;
      }
      else{
        this.exchangeTo.name = data1.name;
        this.exchangeTo.img = data1.img;
        this.exchangeTo.usdPricePerOne = data1.usdPricePerOne;
        this.exchangeTo.tradeFee = data1.tradeFee;
      }
      this.setData(this.typeFrom);
    },
    showModalCurrency(type){
      this.$refs.modal.modalCurrency = true;
      this.$refs.modal.exchangeNumber = type;
    },

    setData(type) {
      this.typeFrom = type;
      if (type == 1) {
        this.exchangeResult.countUsd = this.exchangeFrom.count * this.exchangeFrom.usdPricePerOne;
        this.exchangeTo.count = this.exchangeResult.countUsd / this.exchangeTo.usdPricePerOne;
      }
      if (type == 2) {
        this.exchangeResult.countUsd = this.exchangeTo.count * this.exchangeTo.usdPricePerOne;
        this.exchangeFrom.count = this.exchangeResult.countUsd / this.exchangeFrom.usdPricePerOne;
      }

      if (this.exchangeResult.countUsd == 0) {
        this.typeFrom = 0;
        this.exchangeTo.count = null;
        this.exchangeFrom.count = null;
      }
    },
    swap() {
      this.swapStatus = !this.swapStatus;
      if (this.typeFrom == 1) {
        this.exchangeTo.count = this.exchangeFrom.count;
        this.exchangeFrom.count = null;
        this.typeFrom = 2;
      } else if (this.typeFrom == 2) {
        this.exchangeFrom.count = this.exchangeTo.count;
        this.exchangeTo.count = null;
        this.typeFrom = 1;
      }
      this.setData(this.typeFrom);
    },
    showModalWallet(){
      this.$nuxt.$emit('showModalConnectWallet');
    }
  },
  mounted(){

  },
  name: "Swap",
  components: {
    SvgImport,
    Helper,
    SelectToken,
  }
}


</script>

