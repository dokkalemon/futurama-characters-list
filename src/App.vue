<template>
  <div id="app" class="">
    
    <Header />

    <Main :characterArray="characterList"/>
  </div>
</template>

<script>
import axios from 'axios'
import Header from '@/components/Header.vue'
import Main from '@/components/Main.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main
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

<style lang="scss">
@import '@/styles/global.scss'

</style>
