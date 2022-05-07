<template>
    
     <div class="moviebox">
         
        <div v-for="movie in movie" :key="movie.id" >
                
                <Movie :movie="movie"/>
        </div>

        

     </div>

</template>

<script>

import Movie from "./Movie.vue"
export default{

    name: 'Moviebox',
    components: {
        Movie
    },
    props: {
        movie: Array
    }

}

</script>


<style>

.moviebox{

    background-color: rgb(144, 168, 188);
    padding: 40px;
    color: gray;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    border:3px solid rgb(29, 70, 127);

}
</style>