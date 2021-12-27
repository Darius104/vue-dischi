<template>
    <main>
        <div class="container">
            <Song v-for="(element, index) in songs.response" :key="index" :details="element" />
        </div>
    </main>
</template>

<script>
import axios from 'axios';
import Song from './Song';

export default {
    name: "ListSongs",
    components: {
        Song
    },
    data: function(){
        return{
            songs: [],
        }
    },

    created: function(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response) => {
            this.songs = response.data;
            console.log(this.songs)
        });
    }
}
</script>

<style lang="scss" scoped>
@import '../style/containers.scss';
</style>