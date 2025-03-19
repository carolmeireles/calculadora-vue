<script setup>

const props = defineProps(["filtrarOperacao", "numero1", "numero2"]);

</script>

<template>

<form>
    <div class="row">
        <div class="col">
            <input type="number" placeholder="Digite um número" @keyup="props.numero1" class="campo" />
            <select @change="props.filtrarOperacao">
                <option value="soma">+</option>
                <option value="subtracao">-</option>
                <option value="multiplicacao">*</option>
                <option value="divisao">/</option>
            </select>
            <input type="number" placeholder="Digite um número" @keyup="props.numero2" class="campo" />
        </div>
    </div>
</form>

</template>

<style scoped>

.campo {
    margin: 10px;
}

</style>