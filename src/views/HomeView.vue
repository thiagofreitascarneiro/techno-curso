<template>
  <div class="home">
  <div>
    <p>Carregando...</p>
  </div>
    <h1>Home</h1>
    <p>{{api}}</p>
  </div>
</template>

<script>
// @ is an alias to /src
import fetchData from '@/mixins/fetchData.js'

export default {
  name: 'HomeView',
  mixins: [fetchData],
 
  created() {
    this.fetchData("/home");
  }
 
}
</script>
