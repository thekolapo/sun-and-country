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
  position: sticky;
  bottom: 12rem;
  width: 100%;
  display: flex;
  justify-content: space-between;

  &__links a:first-child {
    margin-right: 3rem;
  }
}
</style>
