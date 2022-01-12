<template>
    <div class="box">
        <FilterGenre @genreFilter="filtered" />
    <div class="album-wrapper">
        <SingleAlbum v-for="(album, index)  in filtered " :key="index" :details="album"/>
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
            // creo una variabile che prendera il valore passato dal figlio
            selectValue:'',
        };
    },
    created: function() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result) => {
        this.albums = result.data.response;
        });
    },
    methods:{
        // utilizzo computed
        // filter: function(){
        //     // this.albums.genre.forEach(element => {
        //     //     if(element.genre)
        //     // });
        //     alert('test');
        // },
    },
    computed:{
        filtered: function(){
            if(this.selectValue === ''){
                return this.albums;
            }else{
            let filteredArray = [];
            filteredArray = this.albums.filter((element) => {
                return element.genre === this.selectValue;
            });
            return filteredArray;
            }
        }
    }
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