<template>
  <section class="card">
      <div class="img">
          <img src="https://upload.wikimedia.org/wikipedia/en/2/28/Philip_Fry.png" alt="">
      </div>
      <div class="info">
          <h2>Philip Jay Fry</h2>
          <h4><span>Gender:<br></span>Male</h4>
          <h4><span>Spieces:<br></span> Human</h4>
          <h4><span>Occupation:<br></span> Intergalatic Delivery Boy</h4>
          <h4><span>Age:<br></span> 25</h4>
          <h4><span>Provenience:<br></span> Earth</h4>
      </div>
  </section>
</template>

<script>
export default {
    name: 'Card',
}
</script>

<style lang="scss">
@import '@/styles/vars.scss';

.card {
    height: 400px;
    width: 50%;
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