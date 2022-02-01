<template>
  <div>
    <select name="Genere" id=""
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
            SelectedGenere:""
        }
    }
}
</script>

<style leng="scss" scoped>
    select{
        border: 2px solid #18d860;
        border-radius: 5px;
        background-color: #2e3a46;
        padding: 5px;
        color: white;
        position: absolute;
        top: 15px;
        left: 100px;
    }
</style>