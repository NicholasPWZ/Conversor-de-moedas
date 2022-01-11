<template>

    <b-row align-h="center">
        <b-col md="3" class="mt-5">
            <b-card :title="valueReal" class="text-center" bg-variant="light">
                <p>Cotação do {{moeda}} hoje </p>
                <br>
                <p>Moeda:</p>
                <b-form-select v-model="moedaSelecionada" :options = "options" title="Moeda:">
                    <b-form-select-option>USD(Dolar Americano)</b-form-select-option>
                    <b-form-select-option>EUR(Euro)</b-form-select-option>
                </b-form-select>
            </b-card>
        </b-col>
    </b-row>
</template>
<script>
export default {
    name : "Card",
    
}
</script>
<style>

</style>