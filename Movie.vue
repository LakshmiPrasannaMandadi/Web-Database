<template>
    <!--div v-if="book.published == false"-->

<div class="movie">
    <ul><h1>Title : {{movie.Title}}</h1></ul>
    <ul><h4>Release Date : {{movie.Release_Date}}</h4></ul>
    <ul><h4>Actor : {{movie.Actors[0]}}</h4></ul>
    <ul><h4>Actress : {{movie.Actors[1]}}</h4></ul>
    <ul><h4>Director : {{movie.Director}}</h4></ul>
    <ul><h4>Rating :  {{movie.Rating}}</h4></ul>
    <ul><h4>Length of Movie : {{movie.length}}</h4></ul>
    <ul><h4>Awards : {{movie.Awards}}</h4></ul>

    
    



    </div>
</template>

<script>

export default{
    name: 'Movie',
    props:{
        movie: Array
    }
}
</script>

<style scoped>



h4{
    margin: 2px;
}

.movie{
    background-color: #b8c8ed;
    color:rgb(2, 7, 16);
    padding: 1em;
    border:3px solid rgb(100, 146, 211);
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    width:100%;
    height:250px;
}

</style>