<template>
  <div id="app">
      <headerBlock />
      <promoBlock />
  </div>
</template>

<script>
import headerBlock from "@/components/headerBlock.vue";
import promoBlock from "@/components/promoBlock.vue";
export default {
  name: 'App',
  components: {
    headerBlock,
      promoBlock
  }
}
</script>

<style lang="scss">
    @import "@/styles/global";
</style>
