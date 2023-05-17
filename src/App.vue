<template>
  <div id="app">
      <headerBlock />
      <promoBlock />
      <materialDescBlock />
      <sliderBlock />
      <footerBlock />
  </div>
</template>

<script>
import headerBlock from "@/components/headerBlock.vue";
import promoBlock from "@/components/promoBlock.vue";
import materialDescBlock from "@/components/materialDescBlock.vue";
import sliderBlock from "@/components/sliderBlock.vue";
import footerBlock from "@/components/footerBlock";
export default {
  name: 'App',
  components: {
      headerBlock,
      promoBlock,
      materialDescBlock,
      sliderBlock,
      footerBlock
  }
}
</script>

<style lang="scss">
    @import "@/styles/global";
</style>
