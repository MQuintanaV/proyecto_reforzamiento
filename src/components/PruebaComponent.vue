<template>
    <div id="PruebaComponent">
        <h1>Prueba</h1>
        <HijoComponent 
        v-bind:mensaje=elsaludo 
        v-bind:despedida= ladespedida
        v-on:eventoParaPadre = "procesar_evento"
        ></HijoComponent>
        <p> 20-7-23</p>
        <p>mensaje recibido del Hijo: {{ mensajeRecibido }}</p>
       
    </div>


</template>

<script>
import HijoComponent from '@/components/HijoComponent.vue';
export default{
    name:'PruebaComponent',
    components:{
        HijoComponent,
    },
    data: function(){
        return{
            elsaludo:'Hola a todos!!!!',
            ladespedida:'me voy, adios',
            mensajeRecibido:'',

        }
    },
    methods:{
        procesar_evento:function(valor){
            this.mensajeRecibido = valor;
        }
    },
    computed:{},
    watch:{},
    created(){

    }
}

</script>

<style scoped>
#PruebaComponent{
    background-color: rgba(177, 52, 200, 0.88);
    color:white
}


</style>