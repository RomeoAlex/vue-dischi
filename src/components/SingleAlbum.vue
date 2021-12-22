<template>
    <div class="album-container">
        <img :src="details.poster" :alt="details.title">
        <div class="album-title">
                {{details.title}}
            </div>
            <div class="author">
                {{details.author}}
            </div>
            <div class="date">
                {{details.year}}
            </div>
    </div>
    
</template>
<script>

export default {
    name:'SingleAlbum',
    props: {
        details: Object
    }
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