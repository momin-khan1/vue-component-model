<script setup>
import { reactive } from 'vue';
import Person from './components/personView.vue'
import MultipleItemView from './components/MultipleItemView.vue';
import ButtonItemView from './components/ButtonItemView.vue';

const person = reactive({
  name: 'Momin Khan',
  age: 25,
  occupation: 'Web Developer'
})

</script>

<template>

<section class="mx-auto container">
  <h1 class="my-10">Component Model</h1>
  <p class="my-5">
    <h2 class="text-xl">Parent</h2>
     {{ person.name }} is {{ person.age }} years old and works as a {{ person.occupation }} .
  </p>

  <Person :person="person" />
  <MultipleItemView v-model:name="person.name" v-model:age="person.age" v-model:occupation="person.occupation" />
  <hr>
  <ButtonItemView v-model:name="person.name" />

</section>

</template>

<style scoped>

</style>
