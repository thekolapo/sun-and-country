<template>
  <div class="app">
    <Nav />
    <Nuxt />
    <Footer />
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
  created() {
    if (process.browser)
      sessionStorage.setItem('triggeredHomepageAnimation', false)
  },
}
</script>

<style lang="scss">
@import '~/assets/scss/main.scss';

.app {
  position: relative;
  width: 92%;
  max-width: 124rem;
  // min-height: 82vh;
  min-height: 90vh;
  margin: 0 auto;
  padding: 0 0rem 8rem;
}
</style>
