<template>
  <v-container class="grey lighten-5 mb-5">
    <v-layout row wrap>
        <v-flex xs12 sm4 md3 xl3 v-bind:key="post.url" v-for="(post, index) in posts" class="pa-2">
            <v-card class="post-card" v-bind:style="{ backgroundImage: 'url(' + post.urlToImage + ')', backgroundSize:'cover', backgroundPosition:'center' }">
                <div class="cover d-flex flex-column justify-end pa-3" :style="coverStyle(index+1)">
                <v-icon :style="{position:'absolute', top:'20px', right:'20px'}"
                dark
                right
                >
                mdi-arrow-right
                </v-icon>
                <span>{{ new Date(post.publishedAt) | dateFormat('DD.MM.YY') }}</span>
                <h3 class="display-0">{{ post.title }}{{++index}}</h3>
                </div>
            </v-card>
        </v-flex>     
    </v-layout>
  </v-container>
</template>

<script>
import Vue from 'vue';
import VueFilterDateFormat from '@vuejs-community/vue-filter-date-format';
Vue.use(VueFilterDateFormat);
export default {
    name:'Posts',
    props:["posts"],
    components:{
       
    },
    data(){
        return{}
    },
    methods:{
        coverStyle:(index) => {
            if(index){
                return
            }
        }
    }
}
</script>

<style scoped>
    .post-card{ min-height:250px; }
    .cover{ width:100%; height:100%; position:absolute; top:0; left:0; }
</style>