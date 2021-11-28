<template>
  <div id="app" class="">
    
    <Header @searchChar="search"/>

    <Main :characterArray="filteredChar"/>
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

    computed: {
      filteredChar() {
        if (this.searchedChar === '') {
          return this.characterList;
        }
         return this.characterList.filter(item => {
           return item.name.first.toLowerCase().includes(this.searchedChar.toLowerCase());
         })
        
      }
    },

    data() {
      return {
        characterList: null,
        searchedChar: '',
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
      },

      search(dato) {
        this.searchedChar = dato;
      }
    }




}
</script>

<style lang="scss">
@import '@/styles/global.scss'

</style>
