<template>
    <div class="album-wrapper">
        <SingleAlbum v-for="(album, index)  in albums " :key="index" :details="album"/>
        
    </div>
</template>
<script>
import axios from 'axios';
import SingleAlbum from "./SingleAlbum.vue";
export default {
    name: 'DiskContainer',
    components: {
        SingleAlbum
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
    }
}
</script>
<style lang="scss" scoped>
.album-wrapper{
    width:70%;
    margin:auto;
    padding-top: 20px;
    display: flex;
    flex-wrap: wrap;    
}
</style>