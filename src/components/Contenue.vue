<template>
    <div class="container mt-5"> 
        <h1 >{{ titre }} </h1>
        <liste :myArr="myArr" @wewe="changementTitre($event)"></liste>
    </div>

</template>

<script>
import Liste from './Liste/Liste.vue'

    export default {
        data(){
            return {
                myArr : [
                    { titre: 'Inception', date: 2010 },
                    { titre: 'Avatar', date: 2009 },
                    { titre: 'Seven', date: 1195 }
                ],
                titre: "Je suis le titre"
            }
        },
        methods: {
            changementTitre(nvTitre){
                this.titre = nvTitre
            }
        },
        components: {
            'liste': Liste
        }
    }
</script>

<style>
h1 {
    margin-top: 100px!important;
}
</style>