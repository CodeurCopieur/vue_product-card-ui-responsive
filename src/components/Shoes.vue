<template lang="pug">
    .main.bg-grid
      Article(v-for="shoe in shoes").card
        .card__img
          //image
          img(:src="shoe.img", :alt="shoe.name")
        .card__name
          p {{ shoe.name }}
        .card__details
          a(href="").card__icon
            ion-icon(name="heart-outline")
          ul.card__wrapper-price
            li.card__price.card__price--before ${{ shoe.priceBefore }}
            li.card__price.card__price--now ${{ shoe.priceNow }}
          a(href="").card__icon 
            ion-icon(name="cart-outline")


</template>

<script>

 export default {
  props: ['shoes'],
  data: () => {
     return {}
   }
  }
</script>

<style lang="scss">

  $first-color: #E3F8FF;
  $second-color: #DCFAFB;
  $third-color: #FFE8DF;
  $accent-color: #FF5151;
  $dark-color: #161616;

  $h3-font-size: 1rem;
  $normal-font-size: 0.938rem;
  $smaller-font-size: 0.75rem;


  
  //layout
  .main {
    padding: 2rem 0;
  }

  .bg-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    max-width: 1200px;
    margin-left: 2.5rem;
    margin-right: 2.5rem;
    align-items: center;
    gap: 2rem;
  }

  //Component
  .card {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 1.5rem 2rem;
    border-radius: 1rem;
    cursor: pointer;
    overflow: hidden;
    transition: .5s;

    &:hover {
      box-shadow: 0 .5rem 1rem #D1D9E6;
    }
    
    &:hover .card__name {
      left: 0;
    }

    &:hover .card__img{
      transform: rotate(30deg);
      margin-left: 3.5rem;
    }

    &:hover .card__details {
      margin-left: 3.5rem;
      padding: 0 1.5rem;
    }

    &:nth-child(1) {
      background-color: $first-color;
    }

    &:nth-child(2) {
      background-color: $second-color;
    }

    &:nth-child(3) {
      background-color: $third-color;
    }

    &:nth-child(4) {
      background-color: $second-color;
    }

    .card__img {
      width: 180px;
      height: auto;
      padding: 3rem 0;
      transition: .5s;
    }

    .card__name {
      position: absolute;
      text-align: center;
      left: -30%;
      top: 0;
      width: 3.5rem;
      height: 100%;
      writing-mode: vertical-lr;
      transform: rotate(180deg);
      background-color: $dark-color;
      color: #ffffff;
      font-weight: bold;
      transition: .5s;
    }

    .card__details {

      width: 100%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      transition: .5s;

      .card__icon {
        font-size: 1.5rem;
        color: $dark-color;
        &:hover ion-icon {
          color: $accent-color;
        }
      }

      .card__wrapper-price {

        .card__price {
          text-align: center;
        }
        .card__price--before  {
          font-size: $smaller-font-size;
          color: $accent-color;
          margin-bottom: .25rem;
        }
        .card__price--now {
          font-size: $h3-font-size;
          font-weight: bold;
        }
      }
    }
  }
</style>