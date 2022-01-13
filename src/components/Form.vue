<template>
    <b-container>
     <b-row align-h="center">
      <b-col md="5" class="mt-5">
        <h4>Faça a conversão de valores</h4>
        <br>
        
        <b-form-group label="Valor a ser convertido:">
        <b-button-toolbar >
        <b-input-group prepend="moedaSelecionada " >
            <b-form-input type="number" :variavel="numeroAConverter"></b-form-input>
            <b-button variant="primary" @click="converter">Converter</b-button>
        </b-input-group>
        </b-button-toolbar>
        </b-form-group>
        <b-form-group label="Valor em reais:" class="mt-3">
           <b-input-group prepend="BR - R$">
            <b-form-input disabled="disabled">{{valorConvertido}}</b-form-input>
           </b-input-group>
        </b-form-group>
      </b-col>        
     </b-row>
    </b-container>
    
</template>
<script>
export default {
    name: "Form", 
    data: function(){
      return{
      currency:[],
      

    }
    },
    props: {
      converter: Function
    
    },
    methods: {
    getDataUsd: async function () {
      const result = await fetch("http://economia.awesomeapi.com.br/json/last/USD-BRL")
        .then((res) => res.json())
        .then((res) => res)
        .catch((error) => {
          const objError = {
            error: true,
            message: error,
          };
          return objError;
        });
      if (!result.error) {
        this.currency = result;
      }
    },
    getDataEur: async function () {
      const result = await fetch("http://economia.awesomeapi.com.br/json/last/EUR-BRL")
        .then((res) => res.json())
        .then((res) => res)
        .catch((error) => {
          const objError = {
            error: true,
            message: error,
          };
          return objError;
        });
      if (!result.error) {
        this.currency = result;
      }
    }
  },
  created: function () {
    this.getData();
  },
  updated: function() {
    this.getMoedaSelecionada( this.moedaSelecionada );
  }
}
    
</script>
<style>

</style>