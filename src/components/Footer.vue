<script>
  import FooterCTA from './partials/FooterCTA.vue';
  import FooterMenu from './partials/FooterMenu.vue';
  import FooterConnect from './partials/FooterConnect.vue';

  export default {
    name: 'Footer',
    components: {
      FooterCTA,
      FooterMenu,
      FooterConnect
    }
  }
</script>

<template>
  <FooterCTA />
  <FooterMenu />
  <FooterConnect />
</template>

<style lang="scss" scoped>

</style>