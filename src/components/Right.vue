<template>
  <div class="right-content">
    <Profile />
    <Friend />
    <Footer />
  </div>
</template>

<script>
import Profile from './Profile.vue';
import Friend from './Friend.vue';
import Footer from './Footer.vue';

export default {
  name: 'Right',
  components:{
    Footer, 
    Profile,
    Friend
  }
}
</script>

<style lang="scss">
  .right-content{
    height: 70vh;
    width: 40vw;
    background-color: red;
  }
</style>