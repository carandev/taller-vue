<script setup>
import CardAreaCuadrado from './components/CardAreaCuadrado.vue'
import CardAreaTriangulo from './components/CardAreaTriangulo.vue'
import CardGrados from './components/CardGrados.vue'
import CardSumaResta from './components/CardSumaResta.vue'
import CardMayorNumero from './components/CardMayorNumero.vue'
import CardAreaCirculo from './components/CardAreaCirculo.vue'
import CardMayoresNumeros from './components/CardMayoresNumeros.vue'
import CardSerie7 from './components/CardSerie7.vue'
import CardMayoresMenoresNumeros from './components/CardMayoresMenoresNumeros.vue'
import CardMayoresMenores3 from './components/CardMayoresMenores3.vue'
import CardMayoresMenores4 from './components/CardMayoresMenores4.vue'
import CardSumatoriaEnteros from './components/CardSumatoriaEnteros.vue'
import CardSumatoriaMultiplos from './components/CardSumatoriaMultiplos.vue'
import CardSumatoriaPares from './components/CardSumatoriaPares.vue'
import CardSumatoriaImpares from './components/CardSumatoriaImpares.vue'
import CardHipotenusa from './components/CardHipotenusa.vue'
import CardAreaCilindro from './components/CardAreaCilindro.vue'
import CardNumeroPar from './components/CardNumeroPar.vue'
import CardRangos from './components/CardRangos.vue'
import CardOrdenar2 from './components/CardOrdenar2.vue'
import CardMultiplos2 from './components/CardMultiplos2.vue'
import CardMinutosHoras from './components/CardMinutosHoras.vue'
import CardEstacionamiento from './components/CardEstacionamiento.vue'
import CardEspectaculo from './components/CardEspectaculo.vue'
import CardKilometrosMetros from './components/CardKilometrosMetros.vue'
import CardNotas from './components/CardNotas.vue'
import CardFactorial from './components/CardFactorial.vue'
import CardPrimo from './components/CardPrimo.vue'
import CardTablaMultiplicar from './components/CardTablaMultiplicar.vue'
import CardNomina from './components/CardNomina.vue'

</script>

<template>
  <h1>Ejercicios de JavaScript</h1>
  <main class="cards">
    <CardAreaCuadrado/>
    <CardAreaCirculo/>
    <CardGrados/>
    <CardSumaResta/>
    <CardMayorNumero/>
    <CardAreaTriangulo/>
    <CardMayoresNumeros/>
    <CardSerie7/>
    <CardMayoresMenoresNumeros/>
    <CardMayoresMenores3/>
    <CardMayoresMenores4/>
    <CardSumatoriaEnteros/>
    <CardSumatoriaMultiplos/>
    <CardSumatoriaPares/>
    <CardSumatoriaImpares/>
    <CardHipotenusa/>
    <CardAreaCilindro/>
    <CardNumeroPar/>
    <CardRangos/>
    <CardOrdenar2/>
    <CardMultiplos2/>
    <CardMinutosHoras/>
    <CardEstacionamiento/>
    <CardEspectaculo/>
    <CardKilometrosMetros/>
    <CardNotas/>
    <CardNomina/>
    <CardFactorial/>
    <CardTablaMultiplicar/>
    <CardPrimo/>
  </main>
</template>

<style>
* {
  box-sizing: border-box;
}
body {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  background-color: #223;
  color: #ddd;
}

h1 {
  text-align: center;
}

.cards {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 2rem;
}

.button {
  padding: .5rem 1rem;
  cursor: pointer;

  background-color: #dd2;
  color: #223;
  border: none;
  outline: none;
  border-radius: 2px;
}

.input {
  padding: .2rem .7rem;
  text-align: center;
  max-width: 100px;
  background-color: transparent;
  border: 1px solid #dd2;
  outline: none;
  color: #ddd;
}

.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 1rem;

  padding: 1rem;

  min-height: 300px;
  min-width: 300px;
  max-width: 500px;

  background-color: #334;
  border-radius: 3px;
}
</style>
