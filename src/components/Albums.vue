<template>
  <div>
    <div class="wrapper" v-if="!loading">
      <Cerca @filtra="filtraalbum"/>
      <div class="container">
          <AlbumItem
          v-for="(elemento, index) in albumFiltrati"
          :key="index"
          :info="elemento"
          />
      </div>
    </div>
    <Loader v-else />
  </div>
</template>

<script>
import axios from "axios"
import AlbumItem from "./AlbumItem.vue"
import Loader from "./Loader.vue"
import Cerca from "./Cerca.vue"

export default {
  name: 'Albums',
      data() {
        return {
            apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
            albumArray: [],
            loading: true,
            nuovoinput:"",
        }
    },
    components: {
      AlbumItem,
      Loader,
      Cerca
    },
    created(){
      this.getPersonaggi();
    },
    computed: {
      albumFiltrati(){
        if(this.nuovoinput == ""){
          return this.albumArray
        }
        return this.albumArray.filter( (info) => {
          return info.genre.includes(this.nuovoinput)
        });
      }
    },
    methods: {
      getPersonaggi(){
        axios
          .get(this.apiURL)
          .then( (risposta) => {
              // handle success
              this.albumArray = risposta.data.response;
              this.loading = false;
          })
          .catch(function (error) {
              // handle error
              console.log(error);
          });
      },
      filtraalbum(album){
        this.nuovoinput = album
        console.log(this.nuovoinput)
      }
    },
  props: {
    
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.wrapper{
  display: flex;
  justify-content: center;
}
.container{
  display: grid;
  grid-template-columns: 300px 300px 300px 300px 300px;

  &>*{
    margin: 0 auto;
    margin-top: 20px;
  }
}

img{
  margin-bottom: 15px;
}

@media screen and (max-width: 1500px){
  .container{
    grid-template-columns: 300px 300px 300px;
  }
}

@media screen and (max-width: 900px){
  .container{
    grid-template-columns:300px 300px;
  }
}

</style>
