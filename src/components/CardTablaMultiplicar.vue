<script setup>
import {ref} from 'vue'

const n = ref(0)
const total = ref([])

function handleClick () {
	for (let i=1; i<=10; i++) {
    total.value.push(i * 5)
	}
}

</script>

<template>
  <section class="card">
    <h3>29. Tabla de multiplicar</h3>
    <label>
      <input type="text" class="input" v-model.number="n">
    </label>
    <button class="button" @click="handleClick">Calcular</button>
    <p><span v-for="(number, index) in total">5 * {{index+1}} = {{number}}<br/></span></p>
  </section>
</template>
