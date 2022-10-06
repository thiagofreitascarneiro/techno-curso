<template>
    <div class="home">
      <h1>Contato</h1>
      {{api}}
    </div>
  </template>
  
  <script>
  // @ is an alias to /src
import fetchData from '@/mixins/fetchData.js'
  
  
  export default {
    name: 'ContatoView',
    mixins: [fetchData],
   
    created() {
        this.fetchData("/contato");
    }
   
  }
  </script>
  