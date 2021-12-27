<template>
    <div class="singleSong">
        <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
        <h2>testo</h2>
        <span>autore + anno</span>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';
    .singleSong{
        background-color: $color_header;
        width: calc(90% / 5);
        height: 350px;
        display: inline-block;
        margin: 10px;
        padding: 30px;
        text-align: center;
        
        img{
            width: 150px;
        }

        h2{
            margin: 10px 0;
            color: $color_word;
        }

        span{
            color: $color_author;
        }
    }
</style>