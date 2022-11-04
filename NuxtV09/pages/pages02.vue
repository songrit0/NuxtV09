<template>
    <h1>{{ demo }}</h1>
</template>

<script>
import { Axios, axios } from 'axios'
import { ref } from 'vue'
export default ({
    data() {
        return {
            demo: 'Hello',
            news:[],
        }
    },
    mounted() {
        const url = `https://newsapi.org/v2/everything?q=tesla&from=2022-10-04&sortBy=publishedAt&apiKey=e50d40f57ef54b4fab3add95a765efa1`
        axios.get(url).then((response) =>{
            console.log(response);
            then.news = response.data
        })

        // const st = [1,2,]
         
        //     const data = async  () => {
        //     const response = await axios.get(`https://newsapi.org/v2/everything?q=tesla&from=2022-10-04&sortBy=publishedAt&apiKey=e50d40f57ef54b4fab3add95a765efa1`)
        //     st.value = response.data.articles
        // }
        // console.log(st);
        // console.log(data);
        // console.log('aa');
        
        
    }, 
})
</script>
