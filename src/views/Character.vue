
<script>
import axios from "axios";
import CharacterCard from '@/components/character-card.vue';
export default {
  components: {
    CharacterCard,

  },
  data() {
    return {
      characters: Object,
    }
  },
  created() {
    axios.get('https://rickandmortyapi.com/api/character').then(data => {
      this.characters = data.data.results
      console.log(data)
    })
  }
}
</script>
<template>
  <div class="characters__wrapper" >
    <CharacterCard v-for="char in characters " :character="char" :key="char.id"></CharacterCard>
  </div>
</template>


<style scoped lang="scss">
.characters__wrapper{
  display: grid;
  grid-template-columns: repeat(4, minmax(1px, 1fr));
  gap: 20px;
}
</style>
