<script setup>
import { ref, computed } from 'vue' 
   
    const contador = ref(0)
const contador2 = ref(0)
const soma = computed(() => contador.value + contador2.value)
const mostrar = ref(true)

</script>

<template>
  <div class="container">
    <button class="btn btn-primary" @click="mostrar= !mostrar">Mostrar e esconder</button>

    <div v-if="mostrar" class="mt-4">
      <div>
        <button class="btn btn-primary" @click="contador--">-</button>
        <span class="mx-3 fs-4">{{ contador }}</span>
        <button class="btn btn-primary" @click="contador++">+</button>
      </div>
      <div>
        <button class="btn btn-primary" @click="contador2--">-</button>
        <span class="mx-3 fs-4">{{ contador2 }}</span>
        <button class="btn btn-primary" @click="contador2++">+</button>
      </div>
    </div>
    <div>
    <p class="fs-3">A soma é {{ soma }}</p>
    <p v-if="soma > 10" class="fs-3">A soma é maior que 10</p>
    <p v-else class="fs-3">A soma é menor ou igual a 10</p>
  
    <div>
      <p v-if="soma % 2 == 0">a soma é par</p>
      <p v-else>a soma é ímpar</p>
    </div>
  </div>
  </div>
   
</template>

<style scoped>


  </style>