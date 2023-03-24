<script setup>
import { ref } from 'vue' ;
   
    const contador = ref(0)
const contador2 = ref(0)
</script>

<template>
   

    <div class="info">
      Contador = {{ contador }}
<button @click="contador++">+</button>
<button @click="contador--">-</button>
<hr>
contador = {{ contador2 }}
<button @click="contador2++">+</button>
<button @click="contador2--">-</button>

</div>
<div class="info">
{{ contador + contador2 }}
<hr>
<div v-if="contador + contador2 > 10" class="verde">Maior que 10</div>
<div v-else-if="contador + contador2 < 10" class="vermelho">Menor que 10</div>
<div v-else>Igual a 10</div>    
<hr>
<div v-if="(contador + contador2) % 2 == 0" >É PAR</div>
<div v-else>É ÍMPAR</div>
</div>
<div v-if="(contador + contador2) % 2==0" class="div2">True</div>
<div v-else class="div1">False</div>
</template>

<style scoped>
.info {
  background-color: rgb(12, 15, 35);
  padding: 20px 30px;
  color: rgb(130, 171, 185);
  border-radius: 20px;
  margin: 5 20px;
}
button{
  margin: 10px;
  border-radius: 10px;
}
.div1{
  background-color: rgb(211, 24, 24);
  padding: 20px 30px;
  color: rgb(0, 7, 9);
  border-radius: 20px;
  margin: 5 20px;
  margin-top: 5px;
}
.div2{
  background-color: rgb(65, 204, 14);
  padding: 20px 30px;
  color: rgb(0, 6, 7);
  border-radius: 20px;
  margin: 5 20px;
  margin-top: 5px;
}
  </style>