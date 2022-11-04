<template>
  <div>
    <!-- <div v-for="(item, index) in news.articles" :key="index">
      <p>{{ item.title }}</p>
    </div> -->


  <div class="contaner mx-auto mt-4 pt-4">
  </div>
  </div>
</template>

<script>
import axios from 'axios'
export default {
    async asyncData() {
        const api ='https://newsapi.org/v2/everything?q=tesla&from=2022-10-04&sortBy=publishedAt&apiKey=ddf082ff7875450fb4a8eacf2b890d71'
        const mountains = await axios.get(api).then((Response)=>{
            return Response.data
        }) 
        return(mountains);
    },



//   data() {
//     return {
//       news: [],
//     };
//   },
//   mounted() {
//     fetch(
//       "https://newsapi.org/v2/everything?q=tesla&from=2022-10-04&sortBy=publishedAt&apiKey=ddf082ff7875450fb4a8eacf2b890d71"
//     ) //api for the get request
//       .then((response) => response.json())
//       .then((data) => {
//         this.news = data;
//         console.log(data);
//       });
//   },
};
</script>

<style>
</style>