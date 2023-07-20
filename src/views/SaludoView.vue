<template>
    <div id="SaludoView">
        <h1>saludo view</h1>
        <p>{{ recibir_nombre }}</p>
    </div>


</template>

<script>
export default{
    name:'SaludoView',
    data: function(){
        return{

        }
    },
    methods:{},
    computed:{
        recibir_nombre:function(){
            return this.$route.params.nombre;
        },
    },
    watch:{},
    created(){

    }
}

</script>

<style scoped>
#SaludoView{
    background-color: lightpink;
}


</style>