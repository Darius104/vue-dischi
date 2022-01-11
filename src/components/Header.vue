<template>
    <header>
        <div class="logo">
            <img src="../assets/spotify.png" alt="logo">
            <select v-model="selectGenre" id="songs" @change="$emit('selectChange', selectGenre)">
                <option value="NaN">All</option>
                <option value="Rock">Rock</option>
                <option value="Pop">Pop</option>
                <option value="Jazz">Jazz</option>
                <option value="Metal">Metal</option>
            </select>
        </div>
    </header>
</template>

<script>
export default {
    name: "Header",
    data: function(){
        return{
            selectGenre: "NaN"
        };
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';
    header{
        height: 70px;
        width: 100%;
        background-color: $color_header;
        display: flex;
        align-items: center;
        margin-bottom: 80px;
        .logo{
            width: 100px;
            display: flex;
        }
        
    }
</style> 