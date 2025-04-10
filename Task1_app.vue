<template>
  <div>
    <h1><strong>Compute Product</strong></h1>
    <img src="https://raw.githubusercontent.com/sabirinID/GE-Aerospace-Software-Engineering-Virtual-Internship/main/Files/1-Build%20a%20user%20interface/Pexels%20Photo.jpeg" alt="Your Image">
    <p>Number 1: <input type="number" v-model="num1"></p>
    <p>Number 2: <input type="number" v-model="num2"></p>
    <button v-if="!computed" @click="computeProduct">Compute</button>
    <p v-else>The product is: {{ product }}</p>
  </div>
</template>

<script setup>
import { ref } from 'vue';

let num1 = ref(5);
let num2 = ref(10);
let product = ref(0);
let computed = ref(false);

const computeProduct = () => {
  product.value = num1.value * num2.value;
  computed.value = true;
}
</script>
