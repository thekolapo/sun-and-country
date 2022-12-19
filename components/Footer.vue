<template>
  <footer ref="footer" class="footer">
    <div class="footer__copyright">Vistanium © 2022</div>
    <div class="footer__links">
      <a class="c-link" href="https://twitter.com/Vistanium" target="_blank">
        Twitter
      </a>
      <a
        class="c-link"
        href="https://www.instagram.com/vistanium/?hl=en"
        target="_blank"
      >
        Instagram
      </a>
    </div>
  </footer>
</template>

<script>
export default {
  watch: {
    $route(to, from) {
      this.setBackgroundColor()
    },
  },
  mounted() {
    this.setBackgroundColor()
  },
  methods: {
    setBackgroundColor() {
      if (
        this.$route.path.includes('team') ||
        this.$route.path.includes('vision')
      ) {
        setTimeout(() => {
          this.$refs.footer.style.setProperty('--background', 'white')
        }, 600)
      } else this.$refs.footer.style.setProperty('--background', 'transparent')
    },
  },
}
</script>

<style lang="scss" scoped>
.footer {
  --background: transparent;
  position: fixed;
  bottom: 0rem;
  padding-bottom: 4rem;
  width: inherit;
  max-width: inherit;
  display: flex;
  justify-content: space-between;

  @include screen(med) {
    // background: $color-dark;
    bottom: 0rem;
    padding: 1.5rem 0 2rem;
    background: var(--background);
  }

  @include screen(small) {
    font-size: 1.7rem;
  }

  &__links a:first-child {
    margin-right: 3rem;

    @include screen(small) {
      margin-right: 1.6rem;
    }
  }
}
</style>
