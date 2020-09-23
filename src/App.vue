<template lang="pug">
  #app
    h1.titre-shop SHOP
    .main.bg-grid
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

  $first-color: #E3F8FF;
  $second-color: #DCFAFB;
  $third-color: #FFE8DF;
  $accent-color: #FF5151;
  $dark-color: #161616;


/*Tipografia responsive*/
  $body-font: 'Open Sans';
  $h1-font-size: 1.5rem;
  $h3-font-size: 1rem;
  $normal-font-size: 0.938rem;
  $smaller-font-size: 0.75rem;

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

ul{list-style:none;padding: 0;}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

  //layout
  .main {
    padding: 2rem 0;
  }

  .bg-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minimax(220px, 1fr));
    max-width: 1200px;
    margin-left: 2.5rem;
    margin-right: 2.5rem;
    align-items: center;
  }
}
</style>
