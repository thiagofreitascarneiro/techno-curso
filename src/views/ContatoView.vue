<template>
    <div>
        
        <div v-if="loading">
            <PageLoading/>
        </div>
        <transition>
            <div v-if="api">
                <h1>{{api.titulo}}</h1>
                <p>{{api.descricao}}</p>
                <ul>
                    <li>
                        <b>Email: </b>
                        {{api.contato.email}}
                    </li>
                </ul>
                <ul>
                    <li>
                        <b>Telefone:</b>
                        {{api.contato.telefone}}
                    </li>
                </ul>
                <ul>
                    <li>
                        <b>Endereço: </b>
                        {{api.contato.endereco}}
                    </li>
                </ul>
            </div>
        </transition>
       
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
  