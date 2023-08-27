<script setup>

const props = defineProps(['name'])
const emit = defineEmits('update:name')

const updateValue = () => {
    emit('update:name', props.name.split('').reverse().join(''))
}

</script>

<template>
    <h2 class="text-2xl mb-5">Button Item</h2>
    <button @click="updateValue()" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">Update</button>
</template>

<style scoped></style>