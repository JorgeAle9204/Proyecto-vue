<template>
    
    <h3>La temperatutra actual en la CDMX es: {{ weatherStore.temperatura }}C° </h3>

</template>

<script setup>
import {useWeather} from '../composables/useWeather';
import {onMounted} from 'vue';
import {useWeatherStore} from '../stores/weatherStore'; 

const weatherStore = useWeatherStore();

onMounted (() => {
useWeather();
})

</script>

<style scoped>

</style>