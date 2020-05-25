<template>
    <div id="caixa">
        <input type="text" placeholder="Nova Tarefa?" class="placeHolder" v-model="texto">
        <button class="button" @click="acrescentar">OK</button>
    </div>
</template>

<script>
export default {
    name : 'Caixas',
    data: function(){
        return{
            texto: ''
        }
    }, methods: {
        acrescentar: function(){
            this.$emit('acrescentar', {texto: this.texto})
            this.texto = "";
        }
    }
}
</script>

<style>
    #caixa{
        width: 300px;
        height: 120px;
        margin: 30px auto 10px auto;
        display: flex;
        flex-wrap: wrap;
    }
    .placeHolder{
        width: 200px;
        height: 20px;
        margin: 50px 0 0 50px;
    }
    .button{
        height: 26px;
        margin-top: 50px;
        background-color: green;
        border: 0;
        outline: none;
        color: #ffff    ;
    }
</style>