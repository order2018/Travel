<template>
  <div class="city">
      <city-header></city-header>
      <city-search></city-search>
  </div>
</template>

<script>
import CityHeader from './components/Header'
import CitySearch from './components/Search'
export default {
  name: 'City',
  data () {
    return {

    }
  },
  components: {
      CityHeader,
      CitySearch
  },
  methods: {

  },
  mounted() {

  }
}
</script>

<style lang="stylus" scoped>

</style>
