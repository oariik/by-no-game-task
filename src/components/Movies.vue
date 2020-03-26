<template>
<div>

<v-card
    class="card"
    max-width="400">

    <v-img
      class="white--text align-end"
      height="200px"
      src="https://picsum.photos/id/0/5616/3744">

      <v-card-title id="title">{{movies[0].author}}</v-card-title>
    </v-img>

     <v-img
      class="white--text align-end"
      height="200px"
      src="https://picsum.photos/id/1001/5616/3744">
      
      <v-card-title id="title">{{movies[3].author}}</v-card-title>
    </v-img>

     <v-img
      class="white--text align-end"
      height="200px"
      hspace="20"
      src= "https://picsum.photos/id/1002/4312/2868">
      
      <v-card-title id="title">{{movies[2].author}}</v-card-title>
    </v-img> 

    
  </v-card> <br/> <br/>
 <hr  id="hr"/>

 <v-card
    class="card"
    max-width="400">

    <v-img
      class="white--text align-end"
      height="200px"
      src=  "https://picsum.photos/id/1003/1181/1772">

      <v-card-title id="title">{{movies[4].author}}</v-card-title>
    </v-img>

     <v-img
      class="white--text align-end"
      height="200px"
      src= "https://picsum.photos/id/1005/5760/3840">
      
      <v-card-title id="title">{{movies[5].author}}</v-card-title>
    </v-img>

     <v-img
      class="white--text align-end"
      height="200px"
      hspace="20"
      src=https://i.picsum.photos/id/1004/5616/3744.jpg>
      
      <v-card-title id="title">{{movies[6].author}}</v-card-title>
    </v-img> 

    
  </v-card>
 </div>


</template>

<script>
  import axios from "axios";

  
 export default {
    created() {
      this.getPosts();
    },
    data() {
      return {
        movies: [],
      };
    },
    methods: {
      getPosts() {
        axios
          .get("https://picsum.photos/v2/list?page=1&limit=10")
          .then(response => (this.movies = response.data))
          .catch(error => {
            this.errors.push(error);
          });
      }
    }
  };
</script>

<style scoped>
 .card {
  display: flex;
  margin-top:40px;
  margin-left:30px;
}

#title {
  color: white;
  font-size: 27px;
  margin-top:120px;
  margin-right:42px;
}

.items{
  display: flex;
}

#hr {
  border: 0.5px dashed black;
}
</style>
