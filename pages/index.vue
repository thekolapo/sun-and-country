<template>
  <div class="home"></div>
</template>

<style lang="scss" scoped>
.home {
  section {
    margin-bottom: 20rem;

    @include screen('small') {
      margin-bottom: 12rem;
    }
  }

  &__hero {
    max-width: 126rem;

    &-subtext {
      margin: 3rem 0 7rem;
      max-width: 87rem;

      @include screen('small') {
        margin: 2.2rem 0 3.2rem;
      }
    }
  }

  &__offers {
    &-list {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      margin-top: 8rem;

      @include screen('small') {
        margin-top: 5rem;
      }
    }

    &-offer {
      width: 46%;
      margin-bottom: 10rem;

      .u-font-h3 {
        margin-bottom: 2.5rem;
        text-transform: uppercase;
      }

      &:nth-child(3),
      &:last-child {
        margin-bottom: 0;
      }

      @include screen('med-small') {
        $margin-bottom: 6rem;
        width: 100%;
        margin-bottom: $margin-bottom;

        &:nth-child(3) {
          margin-bottom: $margin-bottom;
        }
      }
    }
  }

  &__steps {
    &-list {
      display: flex;
      justify-content: space-between;
      flex-wrap: wrap;
      margin-top: 8rem;

      @include screen('small') {
        margin-top: 5rem;
      }
    }

    &-step {
      width: 28%;

      @include screen('med') {
        svg {
          height: fit-content;
        }

        &:first-child svg {
          width: 6rem;
          height: 5.4rem;
        }

        &:nth-child(2) svg {
          width: 11rem;
          height: 5rem;
        }

        &:last-child svg {
          width: 8rem;
          height: 6.2rem;
        }
      }

      @include screen('med-small') {
        width: 100%;

        &:not(:last-child) {
          margin-bottom: 6rem;
        }
      }

      .u-font-h3 {
        margin: 2.5rem 0;
        text-transform: uppercase;
      }
    }
  }

  &__offers,
  &__steps {
    .u-font-h3 {
      @include screen('med-small') {
        margin-bottom: 1.6rem;
      }
    }
  }
}
</style>
