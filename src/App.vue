<script setup>
import Weather from './components/Weather.vue'
</script>

<script>
export default {
  name: "weather-list",
  data() {
    return {
      weatherList: null
    };
  },
  async created() {
    const response = await fetch(import.meta.env.VITE_API_ENDPOINT+"weatherforecast")
    const weatherData = await response.json();
    this.weatherList = weatherData;
  }
};
</script>

<template>
  <div> Testing deployment </div>
  <p>Hi, your weather: </p>
  <p v-for="weather in weatherList">
    <Weather :date="weather.date" :temperatureC="weather.temperatureC" :summary="weather.summary"
      :temperatureF="weather.temperatureF" />
  </p>
</template>
