<template>
    <div class="album-container">
        <img src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
        <div class="album-title">
                Titolo album
            </div>
            <div class="author">
                Autore 
            </div>
            <div class="date">
                e data
            </div>
    </div>
    
</template>
<script>
export default {
    name:'Album.vue'
}
</script>

<style lang="scss" scoped>


.album-container{
    width: calc((100% / 5) - 15px);
    min-height: 400px;
    background-color: #2e3a46;
    padding: 30px;
    text-align: center;
    margin-bottom: 20px;
    margin-right:15px;
    .album-title{
        margin-top:15px;
        font-size:30px;
        font-weight: bold;
        color: white;
    }
    .author{
        margin-top:20px;
        font-size: 20px;
        color:#7e7e79;
    }
    .date{
        font-size: 20px;
        color:#7e7e79;
    }
}
</style>