<template>
  <div class="container">
    <!-- #3 must use the component-->
    <Header TitleName="MOVIE COLLECTION"  />
 


    <Moviebox :movie="movie"  />
    <div class="About">
    <h1> <button><a href="https://nodejs-mandadi-final.herokuapp.com/"> About Me </a></button> </h1>

    </div>


  </div>
</template>
<script>



//import HelloWorld from './components/HelloWorld.vue'
// 1
import Header from './components/Header.vue'
import Moviebox from './components/Moviebox.vue'



// data url: http://localhost:5555/books , this might be different for you
export default {
  name: 'App',
  components: {
    // 2 register the component 
    Header,
    Moviebox
  },

  data(){
    return {
      movie: []
    }
  },
  methods: {
    // promises

      async fetchmovie(){
        const res= await fetch('https://nodejs-mandadi-final.herokuapp.com/api')
         //const res= await fetch('http://localhost:5555/movie')
         const data= await res.json()
          console.log(data)
         return data
      }

  },

  async created(){
    this.movie = await this.fetchmovie()
  }
}
</script>










<style>


@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0px;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 40px;
  border-radius: 5px;
  width:100%;
  background-color: cadetblue;
}

div{
  margin-bottom: 0.5em;
  padding:10px;
}
.About{
  width:100%;
}
a{
    text-decoration: none;
    color: rgb(2, 7, 16);

}
button{
    font-size:30px;
    font-family:'Times New Roman', Times, serif;
    background-color: rgb(102, 147, 176);
    width:100%;
    border:3px solid rgb(46, 99, 173);


}



</style>


