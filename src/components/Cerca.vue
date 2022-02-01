<template>
  <div class="wrapper">
    <div>Generi:</div>
    <select name="Genere" id="select"
    v-model="SelectedGenere"
    @change="$emit('filtra', SelectedGenere)">
        <option value="">All</option>
        <option value="Pop">Pop</option>
        <option value="Rock">Rock</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
    </select>
  </div>
</template>

<script>

export default {
    name: "Cerca",

    props:{

    },

    component:{
        
    },

    data(){
        return{
            SelectedGenere:"",
        }
    }
}
</script>
<style lang="scss" scoped>
    .wrapper{
        position: absolute;
        top: 15px;  
        left: 150px;
        display: flex;
        align-items: center;
    }
    select{
        border: 2px solid #18d860;
        border-radius: 5px;
        background-color: #2e3a46;
        padding: 5px;
        color: white;
        margin-left: 10px;
        width: 100px;
    }
    
</style>