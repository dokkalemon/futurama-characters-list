<template>
  <section class="card">
      <div class="img">
          <img :src="thumb" alt="">
      </div>
      <div class="info">
          <h2>{{ firstName }} {{ middleName }} {{ lastName }}</h2>
          <h4><span>Gender:<br></span> {{ gender }}</h4>
          <h4><span>Spieces:<br></span> {{ species }}</h4>
          <h4><span>Occupation:<br></span> {{ occupation }}</h4>
          <h4><span>Age:<br></span> {{ age }}</h4>
          <h4><span>Provenience:<br></span> {{ provenience }}</h4>
      </div>
  </section>
</template>

<script>
export default {
    name: 'Card',

    props: {
        thumb: String,
        firstName: String,
        middleName: String,
        lastName: String,
        gender: String,
        species: String,
        occupation: String,
        age: String,
        provenience: String,
    }
}
</script>

<style lang="scss">
@import '@/styles/vars.scss';

.card {
    height: 400px;
    width: 49%;
    border: 4px solid $primary-color;
    cursor: pointer;
    transition: all 0.1s ease;
    margin: 5px;
    display: flex;
    &:hover {
        background-image: $card-gradient;
        transform: scale(1.03)
    }
    .img {
        padding: 10px;
        height: 100%;
        width: 50%;
        text-align: center;
    }
    .info {
        height: 100%;
        width: 50%;
        display: flex;
        flex-direction: column;
        text-align: center;
        justify-content: center;
        align-items: center;
    }

    h4 {
        padding: 10px 0;
        font-weight: 400;
        color: white;
        span {
            color: $text-color;
        }
    }
    h5 {
        color: $text-color;
    }

}


</style>