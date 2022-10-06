<template>
    <div>
      <div v-if="loading">
        <PageLoading/>
      </div>
      <div v-if="api">
        <h1>Cursos</h1>
        {{api}}
      </div>
     
    </div>
</template>
  
  <script>
  // @ is an alias to /src
  import fetchData from "@/mixins/fetchData.js"
  
  
  export default {
    name: 'CursosView',
    mixins: [fetchData],
    created() {
        this.fetchData("/cursos")
    }  
  }

  </script>
  