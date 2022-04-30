<script setup>
import {ref} from 'vue'

const hours = ref(5)
const minutes = ref(hours.value * 60)

</script>
<template>
  <section class="card">
    <h3>22. Cuántos minutos hay en 5 horas</h3>
    <p>En {{hours}} horas hay {{minutes}} minutos</p>
  </section>
</template>
