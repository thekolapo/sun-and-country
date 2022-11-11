<template>
  <div class="team">
    <div class="team__role">
      <p class="team__role-title">Research & Story Development</p>
      <div class="team__role-contributors">
        <p>Kosisochukwu Ugwuede</p>
        <p>Beatrice Enyidah</p>
        <p>Aishat Wahab</p>
        <p>Farouq Oyebiyi</p>
        <p>Chinyere Asonta</p>
        <p>Olamide Adio Olanrewaju</p>
        <p>Hauwa Shafii</p>
        <p>Alexander Onukwue</p>
        <p>Aisha Obiagwu</p>
        <p>Oluchi Buchi-Njere</p>
        <p>Habeeb Lanlehin</p>
        <p>Precious Afolabi</p>
        <p>Firdausi Atta</p>
        <p>Aishah Abdulquadri</p>
        <p>Ruth Zakari</p>
        <p>Oritsejolomi Otomewo</p>
        <p>Oyinkonsola Oladeinde</p>
        <p>Samuel Banjoko</p>
      </div>
    </div>
    <div class="team__role">
      <p class="team__role-title">Product & Design</p>
      <div class="team__role-contributors">
        <p>Seyi Olusanya</p>
        <p>Ted Oladele</p>
        <p>Maryam Omoyele</p>
        <p>Okunade Goodman</p>
        <p>Kolapo Oni</p>
      </div>
    </div>
    <div class="team__role">
      <p class="team__role-title">Operations</p>
      <div class="team__role-contributors">
        <p>Tosin Adeyemi</p>
        <p>Ifeyinwa Ogbue</p>
        <p>Anita Eboigbe</p>
        <p>Fu'ad Lawal</p>
      </div>
    </div>
    <div class="team__role">
      <p class="team__role-title">Production</p>
      <div class="team__role-contributors">
        <p>Aisha Salaudeen</p>
        <p>Kayode Idowu</p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.team {
  margin: 7rem auto 0;
  max-width: 55rem;

  &__role {
    display: flex;
    justify-content: space-between;

    &:not(:last-child) {
      margin-bottom: 4rem;
    }

    &-title {
      text-align: right;
      max-width: 27.4rem;
      width: 50%;
      color: wheat;
    }

    &-contributors {
      width: 45%;
      max-width: 22.5rem;
    }
  }
}
</style>
