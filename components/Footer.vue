<template>
  <footer class="footer">
    <div class="footer__copyright">Vistanium © 2022</div>
    <div class="footer__links">
      <a class="c-link" href="" target="_blank">Twitter</a>
      <a class="c-link" href="" target="_blank">Instagram</a>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
.footer {
  position: fixed;
  bottom: 10rem;
  width: inherit;
  max-width: inherit;
  display: flex;
  justify-content: space-between;

  @include screen(med) {
    // background: $color-dark;
    bottom: 0rem;
    padding: 1.5rem 0 2rem;
  }

  &__links a:first-child {
    margin-right: 3rem;

    @include screen(small) {
      margin-right: 2rem;
    }
  }
}
</style>
