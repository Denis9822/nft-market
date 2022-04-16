<template>
  <div class="help_wrap details">
    <img @mouseover="hover = true" @mouseleave="hover = false" v-if="typeImg == 1" :src="'/images/' + nameImg" alt="">
    <SvgImport @icon-hover="hover = true" @icon-leave="hover = false" v-if="typeImg==2" :name="nameImg" />

    <div @mouseover="hover = true" @mouseleave="hover = false" v-show="hover == true" class="hidden">
        <span>Multiplayer</span>
        <p>{{text}}x</p>
      <a href="">
        <div class="contract">
            <h4>
              View contract
            </h4>
          <img src="/images/contract.png" alt="">
        </div>
      </a>
    </div>
  </div>
</template>


<script>
import SvgImport from '~/components/layout/SvgImport'
export default {
  props: {
    typeImg: { type: String, default: "1" },
    nameImg: { type: String, default: "image" },
    text: { type: String, default: "7.21" },
  },
  data() {
    return {
      hover: false,
    }
  },
  methods: {
    consoles() {
     console.log("check");
    },
    handleClick() {
      this.$emit('click');
      console.log("check");
    }
  },
  components:{
    SvgImport,
  }
};
</script>

