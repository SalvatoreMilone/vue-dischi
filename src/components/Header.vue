<template>
  <div class="">
    <div class="container">
      <img src="../assets/img/Spotify_logo.png" alt="">
    </div>
  </div>
</template>

<script>


export default {
  name: 'Header',
  props: {
  },
  data(){
    return{
    }
  },
  components: {

  },
  methods: {

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.container{
  background-color: #2e3a46;
  height: 60px;
  display: flex;
  align-items: center;
  padding: 0 10px;
  margin-bottom: 50px ;
  & img{
    height: 40px;
  }
}
</style>
