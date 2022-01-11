<template>
    <b-container>
     <b-row align-h="center">
      <b-col md="5" class="mt-5">
        <h4>Faça a conversão de valores</h4>
        <br>
        
        <b-form-group label="Valor a ser convertido:">
        <b-button-toolbar >
        <b-input-group prepend= "USD - $" >
            <b-form-input :variavel="numeroAConverter"></b-form-input>
            <b-button variant="primary">Converter</b-button>
        </b-input-group>
        </b-button-toolbar>
        </b-form-group>
        <b-form-group label="Valor em reais:" class="mt-3">
           <b-input-group prepend="BR - R$">
            <b-form-input disabled="disabled"></b-form-input>
           </b-input-group>
        </b-form-group>
      </b-col>        
     </b-row>
    </b-container>
    
</template>
<script>
export default {
    name: "Form",
}
    
</script>
<style>

</style>