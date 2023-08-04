<script setup>
import useClima from "../composables/useClima";

const { formatearTempKtoC } = useClima();

defineProps({
  clima: {
    type: Object,
    required: true,
  },
});
</script>

<template>
  <div class="resultado">
    <h2>Clima de: {{ clima.name }}</h2>
    <p class="actual">{{ formatearTempKtoC(clima.main.temp) }} &deg;C</p>
    <div class="temperaturas">
      <p>
        Min: {{ formatearTempKtoC(clima.main.temp_min) }} <span>&deg;C</span>
      </p>
      <p>
        Max: {{ formatearTempKtoC(clima.main.temp_max) }} <span>&deg;C</span>
      </p>
    </div>
  </div>
</template>
