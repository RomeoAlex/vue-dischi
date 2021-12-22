<template>
    <div class="album-wrapper">
        <Album />
    </div>
</template>
<script>
import axios from 'axios';
import Album from "./Album.vue";
export default {
    name: 'DiskContainer',
    components: {
        Album
        },
    data: function(){
        return {
            albums: [],
        };
    },
    created: function() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result) => {
        
            console.log(result)
        });
    }
}
</script>
<style lang="scss" scoped>
.album-wrapper{
    width:60%;
    margin:auto;

    background-color: pink;
    height:600px;
      
}
</style>