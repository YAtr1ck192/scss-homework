<template>
  <div id="app">
      <headerBlock />
      <promoBlock />
      <materialDescBlock />
  </div>
</template>

<script>
import headerBlock from "@/components/headerBlock.vue";
import promoBlock from "@/components/promoBlock.vue";
import materialDescBlock from "@/components/materialDescBlock.vue";
export default {
  name: 'App',
  components: {
      headerBlock,
      promoBlock,
      materialDescBlock
  }
}
</script>

<style lang="scss">
    @import "@/styles/global";
</style>
