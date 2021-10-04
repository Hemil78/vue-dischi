<template>
    <div class="box-select">
        <select name="" id="">
            <option value="">Seleziona una categoria</option>
            <option value="">Rock</option>
            <option value="">Pop</option>
            <option value="">Jazz</option>
            <option value="">Metal</option>
        </select>
    </div>
</template>

<script>
export default {
    name: "Select",
    
    data() {
       return {
           
       } 
    }
    
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
        border-radius: 8px;
        background-color: $BGcolorHeader;
        color: $ColorSmallText;
    }
}

</style>