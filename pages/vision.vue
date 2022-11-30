<template>
  <div class="vision">
    <h1>This Is About The Most Pivotal Event Since Nigeria’s Independence.</h1>
    <div class="vision__body">
      <p>
        On July 6, 1967, the first shots went off at the Northern border of
        Biafra, a secessionist state that’d broken out of Nigeria a few weeks
        earlier. For the next 20 months, the Nigerian government waged war
        against the secessionist state – the Nigerian Civil War – leading to the
        loss of over one million lives, mainly in the Biafran territory.
      </p>
      <p>
        Sun and Country is the definitive, story-led guide to understanding the
        Nigerian Civil War, capturing the events that led to it, how it played
        out on all sides, and how it continues to shape our world today. Our
        mission is to create a body of work that captures this story and makes
        it accessible to everyone. up.
      </p>
      <p>
        The work we create across multiple formats will ensure that everyone can
        have an informed, nuanced, and kind conversation about the Nigerian
        Civil War.
      </p>
      <p>Fuad Lawal</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.vision {
  margin: 7rem auto 0;
  max-width: 50rem;

  h1 {
    font-size: 4.8rem;
    line-height: 4.8rem;

    @include screen(small) {
      font-size: 3.6rem;
      line-height: 3.6rem;
    }
  }

  &__body {
    margin-top: 5rem;

    @include screen(small) {
      margin-top: 3rem;
    }

    p:not(:last-child) {
      margin-bottom: 3rem;
    }
  }
}
</style>
