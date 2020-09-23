<template lang="pug">
    .wrapper__article
      Article(v-for="shoe in shoes").card
        .card__img
          //image
          img(:src="shoe.img", :alt="shoe.name")
        .card__name
          p {{ shoe.name }}
        .card__details
          a(href="").card__icon
            IosHeartEmptyIcon
          ul
            li.card__price.card__price--before ${{ shoe.priceBefore }}
            li.card__price.card__price--now ${{ shoe.priceNow }}
          a(href="").card__icon 
            IosCartIcon


</template>

<script>

import IosHeartEmptyIcon from 'vue-ionicons/dist/ios-heart-empty.vue'
import IosCartIcon from 'vue-ionicons/dist/ios-cart.vue'

 export default {
  props: ['shoes'],
  components: {
    IosHeartEmptyIcon,
    IosCartIcon
  },
   data: () => {
     return {}
   }
  }
</script>

<style lang="scss" scoped>
  .wrapper__article {
    
    .card {

    }
  }
</style>