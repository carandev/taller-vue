<script setup>
import {ref} from 'vue'

const n = ref(0)
const total = ref(0)

function handleClick () {
  total.value = 1
	for (let i=1; i<=n.value; i++) {
		total.value = total.value * i; 
	}
}

</script>

<template>
  <section class="card">
    <h3>28. Factorial</h3>
    <label>
      <input type="text" class="input" v-model.number="n">
    </label>
    <button class="button" @click="handleClick">Calcular</button>
    <p v-if="total > 0">El factorial es: {{total}}</p>
  </section>
</template>
