<script setup>

const props = defineProps(["filtrarOperacao", "numero1", "numero2"]);

</script>

<template>

<form>
    <input type="number" placeholder="Digite um número" @keyup="props.numero1" />
    <select @change="props.filtrarOperacao">
        <option value="soma">+</option>
        <option value="subtracao">-</option>
        <option value="multiplicacao">*</option>
        <option value="divisao">/</option>
    </select>
    <input type="number" placeholder="Digite um número" @keyup="props.numero2" />
</form>

</template>

<style scoped>

</style>