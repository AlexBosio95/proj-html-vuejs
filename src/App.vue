<template>
  <div id="app">
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue';


export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
  }
}
</script>

<style lang="scss">
@import '~bootstrap/scss/bootstrap.scss';
@import url('https://fonts.googleapis.com/css2?family=Raleway&display=swap');

body{
  font-family: 'Raleway', sans-serif;
  overflow-x: hidden;
  scroll-behavior: smooth;
}
</style>
