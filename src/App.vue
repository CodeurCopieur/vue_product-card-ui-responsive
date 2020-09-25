<template lang="pug">
  #app
    h1.titre-shop SHOP
    app-shoes(:shoes="shoes")
</template>

<script>

import Shoe from './components/Shoes'

export default {
  name: 'App',
  components: {
    'app-shoes': Shoe
  },
  data () {
    return {
      shoes: [
        {
          img: require('./assets/img/img1.png'),
          name: 'AIR ZOOM PEGASUS',
          priceBefore: 990.00,
          priceNow: 749.00
        },
        {
          img: require('./assets/img/img2.png'),
          name: 'AIR ZOOM PEGASUS',
          priceBefore: 990.00,
          priceNow: 749.00
        },
        {
          img: require('./assets/img/img3.png'),
          name: 'AIR ZOOM PEGASUS',
          priceBefore: 990.00,
          priceNow: 749.00
        },
        {
          img: require('./assets/img/img4.png'),
          name: 'AIR ZOOM PEGASUS',
          priceBefore: 990.00,
          priceNow: 749.00
        }
      ]
    }
  }
}
</script>

<style lang="scss">

@import url('https://fonts.googleapis.com/css?family=Open+Sans:400,700&display=swap');

/*-- VARIABLES CSS--*/
/*Colores*/
  $dark-color: #161616;


/*Tipografia responsive*/
  $body-font: 'Open Sans';
  $h1-font-size: 1.5rem;


@media screen and (min-width: 768px){
  
    $h1-font-size: 2rem;
    $normal-font-size: 1rem;
    $smaller-font-size: 0.813rem;
    
}

/*-- BASE --*/
*,::after,::before{
    box-sizing: border-box;
}
body{
    margin: 2rem 0 0 0;
    background-color: #fff;
    color: $dark-color;
    font-family: $body-font;
}
h1{
    font-size: $h1-font-size;
}
img{
    max-width: 100%;
    height: auto;
}
a{
    text-decoration: none;
}

ul{list-style:none;padding:0;margin:0;}

@media screen and (min-width: 1200px){
  body {
    margin: 3rem 0 0 0;
  }

  .titre-shop {
    margin: 0 5rem;
  }

  .bg-grid {
    margin-left: auto;
    margin-right: auto;
  }
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;


  .titre-shop {
    position: relative;
    margin: 0 2.5rem;

    &::after {
      content: "";
      position: absolute;
      top: 50%;
      width: 72px;
      height: 2px;
      background-color: $dark-color;
      margin-left: .25rem;
    }
  }
}
</style>
