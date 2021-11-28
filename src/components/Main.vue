<template>
  <main class="container">



    <Card 
    v-for="(character, index) in characterArray"
    :key="`char${index}`"
    :thumb="character.images.main"
    :firstName="character.name.first"
    :middleName="character.name.middle"
    :lastName="character.name.last"
    :gender="character.gender"
    :species="character.species"
    :occupation="character.occupation"
    :age="character.age"
    :provenience="character.homePlanet"
    />






  </main>
</template>

<script>
/* import axios from 'axios'; */
import Card from '@/components/Card.vue'

export default {
    name: 'Main',
    components: {
      Card,


    },
      props: {
        characterArray: Array,
      }

/*     created() {
      this.takeInfo();
    },

    data() {
      return {
        characterList: null,
      }
    },

    methods: {
      takeInfo() {
        axios.get('https://api.sampleapis.com/futurama/characters')
        .then(result => {
          this.characterList = result.data;
        })
        .catch(err => {
          console.log(err);
        })
      }
    }


 */



}
</script>

<style  lang="scss">
@import '@/styles/vars.scss';

main {
  padding: 20px 0;
  display: flex;
  flex-wrap: wrap;
}

</style>