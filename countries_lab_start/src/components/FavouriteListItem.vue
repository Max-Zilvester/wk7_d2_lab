<template lang="html">
  <div id="favourite_countries">
    <h2>Favourite Countries</h2>
    <p v-for="country in favouriteCountries">{{country.name}}</p>
  </div>
</template>

<script>
export default {
  name: 'favourite-countries',
  props: ['favouriteCountries']
}
</script>

<style lang="css" scoped>
</style>
