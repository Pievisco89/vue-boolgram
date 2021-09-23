<template>
  <div id="app" class="container d-flex"> 
    <div class="leftside">
      <Navbar />

      <Left />
    </div> 

    <Right />
    
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Left from './components/Left.vue';
import Right from './components/Right.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Left,
    Right
  }
}
</script>

<style lang="scss">
@import './assets/styles/general.scss';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
