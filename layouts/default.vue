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
  width: 92%;
  max-width: 124rem;
  min-height: 90vh;
  margin: 0 auto;
  padding: 0 0rem 8rem;
}
</style>
