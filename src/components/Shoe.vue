<template lang="pug">
    .container
      li(v-for="shoe in shoes") {{ shoe.name }}
</template>

<script>
 export default {
  props: ['shoes'],
   data: () => {
     return {}
   }
  }
</script>

<style lang="scss" scoped>
  
</style>