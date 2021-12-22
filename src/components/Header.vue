<template>
    <header>
        <div class="logo">
            <img src="https://upload.wikimedia.org/wikipedia/commons/7/75/Spotify_icon.png" alt="">
            
        </div>
    </header>
</template>
<script>
export default {
    name: 'Header',
};
</script>
<style lang="scss" scoped>


header{
    height: 100px;
    background-color: #2e3a46;
    .logo{
        padding:10px;
        img{
            height: 80px;
        }
    }
}
</style>