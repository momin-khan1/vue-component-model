<script setup>
import SingleItemView from './SingleItemView.vue';


defineProps(['person'])

</script>

<template>

    <p class="my-5">
        <h2 class="text-xl">Child</h2>
        {{ person.name }} is {{ person.age }} years old and works as a {{ person.occupation }} .
    </p>

    <form class="flex flex-col">
        <SingleItemView v-model="person.name" label="Name"/>
        <SingleItemView v-model="person.age" label="Age" />
        <SingleItemView v-model="person.occupation" label="Occupaion" />
    </form>

</template>

<style></style>