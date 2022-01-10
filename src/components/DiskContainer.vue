<template>
    <div class="box">
        <FilterGenre @genreFilter="filter" />
    <div class="album-wrapper">
        <SingleAlbum v-for="(album, index)  in albums " :key="index" :details="album"/>
    </div>
    </div>
</template>
<script>
import axios from 'axios';
import FilterGenre from "./FilterGenre.vue";
import SingleAlbum from "./SingleAlbum.vue";

export default {
    name: 'DiskContainer',
    components: {
        SingleAlbum, 
        FilterGenre,
        },
    data: function(){
        return {
            albums: [],
        };
    },
    created: function() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result) => {
        this.albums = result.data.response;
        });
    },
    methods:{
        filter: function(){
            // this.albums.genre.forEach(element => {
            //     if(element.genre)
            // });
            alert('test');
        },
    },
}
</script>
<style lang="scss" scoped>
.box{
    width: 100%;
    margin: auto;
}
.album-wrapper{
    width:70%;
    margin:auto;
    padding-top: 20px;
    display: flex;
    flex-wrap: wrap;    
}
</style>