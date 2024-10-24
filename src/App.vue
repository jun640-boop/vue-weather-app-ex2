<script setup>
import Navbar from './components/Navbar.vue';
import MainComp from "./components/MainComp.vue";
import {onMounted, ref} from 'vue';
import {useStore} from "vuex";
import About from "./components/About.vue";

const store = useStore();
// 날씨 데이터 상태변수

// 날씨 데이터 가져오기

// 앱이 실행되면 날시 데이터 가져오기
onMounted(() => {
  store.dispatch('getWeather');
})

const onSearchCity = (city) => {
  weatherData.value.city = city;
  getWeather()
}

</script>

<template>
<!--  <button @click="$store.dispatch('getWeather')">getWeather</button>-->
  <Navbar/>
  <div v-if="!$store.state.toggle">
    <MainComp/>
  </div>
  <div v-else>
  <about />
  </div>
</template>

<style scoped lang="scss">

</style>
