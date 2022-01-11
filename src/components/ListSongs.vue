<template>
    <main>
        <div class="container">
            <Song v-for="(element, index) in filterDiscs" :key="index" :details="element" />
        </div>
       
    </main>
</template>

<script>
import axios from 'axios';
import Song from './Song.vue';

export default {
    name: "ListSongs",
    components: {
        Song,
    },
    props: {
        filterGenre: String
    },
    data: function(){
        return{
            songs: [],
        }
    },
    computed: {
        filterDiscs: function(){
            if(this.filterGenre === "NaN"){
                return this.songs;
            }
            let filterArray = [];
            filterArray = this.songs.filter((element) => {
                return element.genre === this.filterGenre;
            });
            return filterArray
        }
    },
    created: function(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((resp) => {
            this.songs = resp.data.response;
        });
    }
}
</script>

<style lang="scss" scoped>
@import '../style/containers.scss';
</style>