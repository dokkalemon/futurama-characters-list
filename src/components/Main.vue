<template>
  <main class="container">
    <Card />
  </main>
</template>

<script>
import Card from '@/components/Card.vue'

export default {
    name: 'Main',
    components: {
      Card
    },







}
</script>

<style  lang="scss">
@import '@/styles/vars.scss';

main {
  padding: 20px 0;
  display: flex;
}

</style>