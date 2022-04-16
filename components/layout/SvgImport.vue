<template>
  <div @mouseover="$emit('icon-hover')" @mouseleave="$emit('icon-leave')" class="svg_wrap" v-html="require(`static/icons/${name}.svg?raw`)" />
</template>


<script>
export default {
  props: {
    name: { type: String, default: "image" },
  },
  methods: {
  },
};
</script>

