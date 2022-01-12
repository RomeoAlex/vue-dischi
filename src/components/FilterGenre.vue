<template>
    <div class="select-box">
        <select @change="$emit('genreFilter', selectValue)" v-model="selectValue" name="" id="genre">
            <option value="">Default</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option>
        </select>
    </div>
</template>
<script>
export default {
    name: 'FilterGenre',
    data: function(){
        return{
            selectValue:'',
        }
    },
    
}
</script>
<style lang="scss" scoped>
.select-box{
    
    padding:30px;
  width:200px;
  margin: auto;
  select{
      padding:10 20;
      width: 200px;
  }
  
}
</style>