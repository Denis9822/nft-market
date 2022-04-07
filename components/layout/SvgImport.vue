<template>
  <div class="svg_wrap" v-html="require(`static/icons/${name}.svg?raw`)" />
</template>


<script>
export default {
  props: {
    name: { type: String, default: "image" },
  },
};
</script>

