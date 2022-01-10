<template>
    <main>
        <Search @passInfo="searchSongs" />
        <div class="container">
            <Song v-for="(element, index) in filterSongs()" :key="index" :details="element" />
        </div>
       
    </main>
</template>

<script>
import axios from 'axios';
import Song from './Song';
import Search from './Search.vue';

export default {
    name: "ListSongs",
    components: {
        Song,
        Search
    },
    data: function(){
        return{
            songs: [],
            serchedText: ''
        }
    },
    methods: {
        searchSongs(selectValue){
            this.serchedText = selectValue;
            console.log(this.serchedText)

        },
// torna array con songs filtrate
        filterSongs: function(){
            
        }
    },

    created: function(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            this.songs = response.data;
        });
    }
}
</script>

<style lang="scss" scoped>
@import '../style/containers.scss';
</style>