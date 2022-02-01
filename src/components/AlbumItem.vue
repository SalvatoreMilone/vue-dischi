<template>
  <div class="">
    <div class="container">
      <img :src="info.poster" alt="alt" height="200px">
      <div>{{info.title}}</div>
      <div>{{info.author}}</div>
      <div>{{info.year}}</div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'AlbumItem',
  props: {
    info: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.container{
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  width: 200px;
  height: 350px;
  padding: 20px;
  background: #2e3a46;
  text-align: center;

  :nth-child(2){
    font-size: 22px;
    font-weight: bold;
    margin-bottom: 5px;
  }

  :nth-child(3){
    color: #999;
  }
  :nth-child(4){
    color: #999;
  }
}

img{
  margin-bottom: 15px;
}

</style>
