<template>
  <div id="app">
    <Header />
    <Main 
    :articlesList = 'articlesList'
    :articlesListAll = 'articlesListAll'/>
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';
import axios from 'axios'


export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
  },
  data: function(){
    return{

      articlesList: [],
      articlesListAll: []
    }
  },

    methods: {

        getArticle(){
          axios.get('https://newsapi.org/v2/top-headlines?country=it&apiKey=8d1549fdace743848d7f961305b0de09')
          .then((result) =>{
            this.articlesListAll = result.data.articles
            console.log(this.articlesListAll)
            this.articlesList = this.articlesListAll.slice(0, 5)

            console.log(this.articlesList)
            
          })
        }
        
      },

    created(){
      this.getArticle()
    }
}
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap.scss';
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');

body{
  font-family: 'Montserrat', sans-serif;
  overflow-x: hidden;
  scroll-behavior: smooth;
}
</style>
