<template>

  <div>
    <div class="box-img">
      <img :src="img"/>
    </div>
    <div class="box-text">
      <h4>{{bigText}}</h4>
      <p>{{smallText}}</p>
      <p>{{dateText}}</p>
    </div>
    
    
  </div>

</template>

<script>
export default {
    name: "Album",
    props: {
      img: String,
      bigText: String,
      smallText: String,
      dateText: String
    }
}
</script>

<style lang="scss" scoped>

@import "../assets/style/common";

.box-img{
  width: 100%;

  img{
    width: 100%;
  }
}
.box-text{

  h4{
        padding: 10px 0;
        color: #fff;
        text-transform: uppercase;
    }

    p{
        color: $ColorSmallText;
        font-size: 14px;
    }
}


</style>



  


