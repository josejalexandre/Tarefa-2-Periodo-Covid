<template>
  <div id="app">
    <caixas @acrescentar="adicionarTarefa($event)"/>
    <lista :tarefas="tarefas" />
  </div>
</template>

<script>
import Caixas from "./components/Caixas.vue"
import Lista from "./components/Lista.vue"
export default {
  name: 'App',
  components: {
    Caixas,
    Lista
  },
  data: function() {
    return {
      tarefas: []
    };
  },
  methods: {
    adicionarTarefa: function(event) {
      this.tarefas.push({descricao: event.texto});
    }
  }
};
</script>

<style>

</style>