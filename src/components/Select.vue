<template>
    <div class="box-select">
        <select name="tipe-music" id="tipe-music" v-model="selectValue" @change="$emit('search', selectValue)">
            <option value="">Seleziona una categoria</option>
            <option :value="genere" v-for="genere in generi" :key="genere">{{genere}}</option>
<!--             <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option> -->
        </select>
    </div>
</template>

<script>
export default {
    name: "Select",
    
    data() {
       return {
           selectValue: ""
       } 
    },
    props: ["generi"]
    
}
</script>

<style lang="scss" scoped>

@import "../assets/style/common";

.box-select{
    
    margin-top: 50px;

    select{
        min-width: 500px;
        padding: 10px;
        border: none;
        background-color: $BGcolorHeader;
        color: $ColorSmallText;
        -moz-appearance: none;
        -webkit-appearance: none;
        appearance: none;
    }
}

</style>