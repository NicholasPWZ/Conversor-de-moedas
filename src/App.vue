<template>
    <div id="app">
    <Header/>
    <b-container>
      <b-col mt="5">
        <Card/>
      </b-col>
    </b-container>
    <br>
    <b-container>
      <Form/>
    </b-container>
    </div>
</template>

<script>
import Header from "./components/Header.vue"
import Card from "./components/Card.vue"
import Form from "./components/Form.vue"

export default {
  name: 'App',
  components: {
    Header,
    Card,
    Form
  },
  data: function(){

  },
  methods:{
    converter : function(){
      this.valorConvertido = (this.ask * this.numeroAConverter).toFixed(2).replace(".",",");
    }
  },
};
</script>

<style>
 
</style>
