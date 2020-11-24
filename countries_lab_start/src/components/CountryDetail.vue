<template lang="html">
  <div id="selected_country">
    <h2> Country Name: {{selectedCountry.name}}</h2>
    <p> Population: {{selectedCountry.population}}  </p>
    <img class="lrg-flag" />

    <neighbouring-countries>
    </neighbouring-countries>

</div>
</template>

<script>
import NeighbourCountry from './NeighbourCountry.vue';
export default {
  name: 'country-detail',
  props: ['selectedCountry'],
  components: {
    'neighbouring-countries': NeighbourCountry
  }
}
</script>

<style lang="css" scoped>

.lrg-flag {
  height: 100px
}

</style>
