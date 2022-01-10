<template>
    <div>
        <select name="cars" id="cars">
            <option value="volvo">All</option>
            <option value="saab">Rock</option>
            <option value="mercedes">Pop</option>
            <option value="audi">Jazz</option>
            <option value="audi">Metal</option>
        </select>
    </div>
</template>

<script>
export default {
    name: "Search"
}
</script>

<style lang="scss" scoped>
select{
    margin-left: 400px;
}
</style>