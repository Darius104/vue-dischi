<template>
    <header>
        <div class="logo">
            <img src="../assets/spotify.png" alt="">
        </div>
    </header>
</template>

<script>
export default {
    name: "Header"
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

        .logo{
            width: 100px;
        }
    }
</style> 