<script setup>

defineProps(['name', 'age', 'occupation'])
defineEmits(['update:name', 'update:age', 'update:occupation'])

</script>

<template>
    <form action="" class="my-5 flex flex-col">
        <label for="">Name</label>
        <input type="text" :value="name" @input="$emit('update:name', $event.target.value)">
        <label for="">Age</label>
        <input type="text" :value="age" @input="$emit('update:age', $event.target.value)">
        <label for="">Name</label>
        <input type="text" :value="occupation" @input="$emit('update:occupation', $event.target.value)">
    </form>
</template>

<style scoped></style>