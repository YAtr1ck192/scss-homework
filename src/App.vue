<template>
  <div id="app">
      <headerBlock />
  </div>
</template>

<script>
import headerBlock from "@/components/headerBlock.vue";
export default {
  name: 'App',
  components: {
    headerBlock
  }
}
</script>

<style lang="scss">
    @import "@/styles/global";
</style>
