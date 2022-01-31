<template>
  <div class="">
    <div class="container">
      <img :src="info.poster" alt="alt" width="200px">
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
  height: 300px;
  padding: 20px;
  background: #2e3a46;
}

img{
  margin-bottom: 15px;
}

</style>
