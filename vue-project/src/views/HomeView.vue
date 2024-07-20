<script setup>
import TheWelcome from '../components/TheWelcome.vue'
import { ref, watch } from 'vue';

let food = ref(localStorage.getItem('food'));
let age = ref(localStorage.getItem('age'));

watch(food, (val) => {
  write('food', val)
})
watch(age, (val) => {
  write('age', val)
})


function write (key, value) {
  localStorage.setItem(key, value);
}

setTimeout(() => {
  food.value = "autofill";
}
, 3000)
</script>

<template>
  <main>
    <!-- <TheWelcome /> -->
    <p>
      Whats your favourite food?<input type="text" v-model="food" @input="write('food', food)">
    </p>

    <p>
      How old are you?<input type="text" v-model="age" @input="write('age',age)">
    </p>

  </main>
</template>
