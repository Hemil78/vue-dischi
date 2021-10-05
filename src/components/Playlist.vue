<template>

  <section class="container">

    <div class="search-album">
        <Select @search="searchEvent" :generi="generi"/>
    </div>

    <div class="box-albums">

        <Album class="object-album" v-for="(elm, index) in genereFilter" :key="index"
            :img="elm.poster"
            :bigText="elm.title"
            :smallText="elm.author"
            :dateText="elm.year"/>    

    </div>

    
  </section>

</template>
      
    

<script> 
import axios from 'axios';            
import Album from './Album.vue';
import Select from './Select.vue';

export default {
    name: "Playlist",
    components: {
        Album,
        Select
    },
    data() {
       return {
           albums: [],
           genere: "",
           generi: []
           
       } 
    },
    created() {
        axios
            .get("https://flynn.boolean.careers/exercises/api/array/music")
            .then( (res) =>{
                this.albums = res.data.response;
                this.albums.forEach(
                    (album) => {
                        if(!this.generi.includes(album.genre)) {
                            this.generi.push(album.genre);
                        }
                    }
                );

            });
    },
    methods: {
        searchEvent(elm) {
            this.genere = elm;
            console.log(elm);
        }
    },
    computed: {
        genereFilter() {
            return this.albums.filter(
                (album) => {
                    if(album.genre == this.genere || this.genere == "") {
                        return true
                    }
                    return false
                }
            );
        }
    }
    
}
</script>

<style lang="scss" scoped>

@import "../assets/style/common";

.search-album{
    width: 100%;
    text-align: center;
}

.box-albums{
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    padding: 40px 0;
}
.object-album{
    width: calc(100% / 5 - 20px);
    text-align: center;
    margin: 10px;
    padding: 15px;
    background-color: $BGcolorHeader;
}    
    
</style>


    

      
             

              

              


