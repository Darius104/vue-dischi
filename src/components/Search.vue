<template>
    <div>
        <select @change="$emit(this.selectValue)" v-model="selectValue" name="cars" id="cars">
            <option value="All">All</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option>
        </select>
    </div>
</template>

<script>
export default {
    name: "Search",
    data: function(){
        return{
            selectValue: ''
        };    
    }
}
</script>

<style lang="scss" scoped>
select{
    margin-left: 400px;
}
</style>