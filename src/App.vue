<template lang="pug">
  #app
    app-shoes(:shoes="shoes")
</template>

<script>

import Shoe from './components/Shoe'

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


@import url('./assets/scss/index.scss');

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
