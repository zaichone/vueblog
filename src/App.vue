<template>
  <v-app>
    <Header/>

    <v-main>
      <v-container class="grey lighten-5">
        <v-row class="text-center">
          <h1 class="mt-2 mb-3">Headlines</h1>
        </v-row>
      </v-container>
    
      <Posts v-bind:posts="this.posts"/>
    </v-main>
  </v-app>
</template>

<script>
//import Vue from 'vue';
import axios from 'axios';
import Header from './components/Header';
import Posts from './components/Posts';




//console.log(response.data);
export default {
  name: 'App',

  components: {
    Header,
    Posts
  }, 
  data(){
    return{
      posts:[]
    }
  },
  methods:{

  },
  created(){
    axios.get('https://newsapi.org/v2/top-headlines?country=us&apiKey=099148be22804e849a0c6fe022b7cf5e')
    .then(res => this.posts = res.data.articles)
    .catch(err => console.log(err));
  }
  
};
</script>