<template>
  <div class="colorTitleStyle">
    <div class="ctColor" />
    <div class="ctTitle">{{ title }}</div>
    <slot name="subTitle"></slot>
    <div style="flex: 1" />
    <div class="ctRight"><slot name="right"></slot></div>
  </div>
</template>
<script>
export default {
  name: "ColorTitle",
  props: {
    title: String,
  },
};
</script>
<style lang="less" scoped>
@import "./css/index.less";
</style>