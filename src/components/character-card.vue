

<script>
import { faPhone } from "@fortawesome/free-solid-svg-icons";
export default {

  props: {
    character: Object
  },
  components: {
  }
}
</script>
<template>
  <div class="character-card">
    <header class="character-card-header">
      <img class="character-card-header__img" :src="character.image
        " :alt="character.name">
      <div class="character-card-header__name-bg">
        <p class="character-card-header__name">{{ character.name }}</p>
      </div>
    </header>
    
    <div>
      <font-awesome-icon v-if="character.gender === 'Male'" icon="mars" style="color: #281cca;" />
      <font-awesome-icon v-else-if="character.gender === 'Female'" icon="venus" />
    </div>
    <p>{{ character.species
    }}</p>

    <p>{{ character.status }}</p>
    <p>{{ character.gender }}</p>
    <p>{{ character.type }}</p>
  </div>
</template>
<style scoped lang="scss" >
.character-card {
  /* display: block; */
  height: 100%;
  /* box-shadow: 1px 1px 1px 1px red; */
  max-width: 216px;
  overflow: hidden;
  object-fit: cover;
  border-radius: 5px;
  border: 1px solid red;

  &-header {
    position: relative;
    display: flex;

    &__name-bg {
      width: 100%;
      background: #070707d7;
      padding: 5px;
      bottom: 0;
      position: absolute;
    }

    &__img {
      width: 100%;
      position: relative;
    }

    &__name {
      font-size: 0.9rem;
      color: white;
      text-align: center;
    }
  }




}
</style>
