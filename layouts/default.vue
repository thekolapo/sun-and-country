<template>
  <div class="app">
    <Nav />
    <Nuxt />
    <Footer />
  </div>
</template>

<style lang="scss">
@import '~/assets/scss/main.scss';

.app {
  position: relative;
  max-width: 124rem;
  margin: 0 auto;
  padding: 4.6rem 0 10rem;
  min-height: 90vh;
}
</style>
