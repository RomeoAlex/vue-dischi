<template>
    <div class="album-wrapper">
        <Album v-for="album  in albums " :key="album" :details="album "/>
        
    </div>
</template>
<script>
import axios from 'axios';
import Album from "./SingleAlbum";
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
    width:60%;
    margin:auto;
    padding-top: 20px;
    display: flex;
    flex-wrap: wrap;    
}
</style>