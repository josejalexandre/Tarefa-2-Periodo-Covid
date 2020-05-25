<template>
    <div id="lista">
        <div class="tarefas" v-for="(lista, index) in tarefas" :key="index">
            {{ lista.descricao }}
        </div>
    </div>
</template>

<script>
export default {
    name: "Lista",
    props: ['tarefas']
}
</script>

<style>
  #lista{
        width: 300px;
        height: 120px;
        border: black 2px solid;
        margin: 30px auto 10px auto;
        display: flex;
        flex-wrap: wrap;
        overflow: auto;
    }
    .tarefas{
        width: tarefas;
        height: 20px;
        border: 1px black solid;
        margin: 2px 2px 2px 2px;
    }
</style>