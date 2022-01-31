<template>
  <div class="hello">
    <Albums/>
  </div>
</template>

<script>
import Albums from './Albums.vue'

export default {
  name: 'Main',
  props: {
    
  },
  components: {
    Albums
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
