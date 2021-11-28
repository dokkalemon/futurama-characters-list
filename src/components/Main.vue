<template>
  <main class="container">
    <Card />
  </main>
</template>

<script>
import axios from 'axios';
import Card from '@/components/Card.vue'

export default {
    name: 'Main',
    components: {
      Card
    },

    created() {
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






}
</script>

<style  lang="scss">
@import '@/styles/vars.scss';

main {
  padding: 20px 0;
  display: flex;
}

</style>