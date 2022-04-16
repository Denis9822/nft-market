<template>
  <div class="help_wrap">
    <img @mouseover="hover = true" @mouseleave="hover = false" v-if="typeImg == 1" :src="'/images/' + nameImg" alt="">
    <SvgImport @icon-hover="hover = true" @icon-leave="hover = false" v-if="typeImg==2" :name="nameImg" />

    <div v-show="hover == true" class="hidden">
        {{text}}
    </div>
  </div>
</template>


<script>
import SvgImport from '~/components/layout/SvgImport'
export default {
  props: {
    typeImg: { type: String, default: "1" },
    nameImg: { type: String, default: "image" },
    text: { type: String, default: "Make a swap on Biswap and get up to 90% of fee return In BSW Tokens." },
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

