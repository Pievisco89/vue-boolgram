<template>
  <div>
    <Header />
    
    <div id="app" class="container d-flex"> 
      <div class="leftside">
        <Navbar />

        <Left />
      </div> 

      <Right />
      
    </div>
  </div>
    
</template>

<script>
import Header from './components/Header.vue';
import Navbar from './components/Navbar.vue';
import Left from './components/Left.vue';
import Right from './components/Right.vue';

export default {
  name: 'App',
  components: {
    Header,
    Navbar,
    Left,
    Right
  }
}
</script>

<style lang="scss">
@import './assets/styles/general.scss';

#app {
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
