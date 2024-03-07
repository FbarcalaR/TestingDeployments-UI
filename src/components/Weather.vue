<script setup>

defineProps({
  date: String,
  summary: String,
  temperatureC: Number,
  temperatureF: Number,
})

</script>

<template>
  <h1>{{ date }}</h1>

  <div>
    <span>summary: </span>
    <span>{{ summary }}</span>
  </div>
  <div>
    <span>temperature: </span>
    <span>{{ temperatureC }}</span>
  </div>
  <div>
    <span>weird temperature (Fahrenheit): </span>
    <span>{{ temperatureF }}</span>
  </div>
</template>
