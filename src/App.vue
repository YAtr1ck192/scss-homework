<template>
  <div id="app">
      <headerBlock />
      <promoBlock />
      <materialDescBlock />
      <sliderBlock />
  </div>
</template>

<script>
import headerBlock from "@/components/headerBlock.vue";
import promoBlock from "@/components/promoBlock.vue";
import materialDescBlock from "@/components/materialDescBlock.vue";
import sliderBlock from "@/components/sliderBlock.vue";
export default {
  name: 'App',
  components: {
      headerBlock,
      promoBlock,
      materialDescBlock,
      sliderBlock
  }
}
</script>

<style lang="scss">
    @import "@/styles/global";
</style>
