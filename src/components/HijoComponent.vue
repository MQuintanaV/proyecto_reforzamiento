<template>
    <div id="HijoComponent">
        <h1>Hijo Component</h1>
        <p>{{ mensaje }}</p>
        <p>{{ despedida }}</p>

        <form>
            <label for="txtRespuesta">Respuesta: </label>
            <input type="text" id="txtRespuesta" v-model= respuesta_hijo>
            <button v-on:click.prevent="enviar_al_padre">enviar al padre</button>
        </form>
        <br>
        <p>{{ respuesta_hijo }}</p>
       
    </div>


</template>

<script>
export default{
    name:'HijoComponent',
    props: ['mensaje','despedida'],
    data: function(){
        return{ 
            respuesta_hijo:'',

        }
    },
    methods:{
        enviar_al_padre: function(){
            this.$emit('eventoParaPadre', this.respuesta_hijo);
        }
    },
    computed:{},
    watch:{},
    created(){

    },
}

</script>

<style scoped>
#HijoComponent{
    background-color: rgba(182, 214, 171, 0.88);
    margin:3%;
}


</style>