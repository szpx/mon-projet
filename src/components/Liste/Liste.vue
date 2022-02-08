<template>
    <div>
        <ul class="liste">
            <li v-for="(film, index) in myArr" :key="index">
                <div class="card">
                    <div class="card-body">
                        Titre : {{ film.titre }}
                        <br>
                        Date : {{ film.date }}
                    </div>
                </div>
            </li>
        </ul>

        <div @click="supprFilm" class="btn btn-danger mt-2">
            Supprime le film
        </div>
        <br>
        <div @mouseover="changeTitre" class="btn btn-danger mt-2">
            Modifie le titre
        </div>
    </div>
</template>

<script>
import { bus } from '../../main.js'
export default {
    name: 'Liste',
    data(){
        return {
            fruits: ['Orange', 'Papaye', 'Fraise'],
            ola: this.myArr
        }
    },
    methods: {
        supprFilm() {
            this.ola.pop()
        },
        changeTitre(){
            // this.$emit('wewe', alert('Mon putain titre'))
            bus.$emit('wewe', alert('Titre changé avec le bus'))
        }
    },    
    props: ['myArr']
}
</script>

<style >
</style>