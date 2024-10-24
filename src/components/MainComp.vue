<template>
  <div class="container">
    <SearchBar />
    <WeatherInfo />

  </div>
</template>

<script setup>
import SearchBar from './SearchBar.vue'
import WeatherInfo from './WeatherInfo.vue';


</script>

<style lang="scss" scoped>

.weather-info{
  padding: 20px;
  & > div {
    margin-bottom: 20px;
    padding: 20px;
    border: 1px solid #ccc;
  }
  .icon img{
    width: 140px;
  }
  .temp{
    font-size: 4px;
  }

}
</style>