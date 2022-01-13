<template>

    <b-row align-h="center">
        <b-col md="3" class="mt-5">
            <b-card :title="moedaSelecionada" class="text-center" bg-variant="light" >
                <p>Cotação do {{moedaSelecionada}} hoje </p>
                    {{moedaSelecionada.ask}}
                <br>
                <p>Moeda:</p>
                <b-form-select v-model="moedaSelecionada" title="Moeda:" >
                    <b-form-select-option value="USD" >USD(Dolar Americano)</b-form-select-option>
                    <b-form-select-option value="EUR" >EUR(Euro)</b-form-select-option>
                </b-form-select>
            </b-card>
        </b-col>
    </b-row>
</template>
<script>
export default {
    name : "Card",
    data: function(){
        return{
            currency:[],
            moedaSelecionada:"USD"
        }
    },
    props:{
     
    }
}
</script>
<style>

</style>