<template>
  <div class="right-content">
    <Profile />

    <div class="friend">
      <h2 class="m-2">Suggerimenti per te</h2>
      <div
        class="d-flex align-items-center justify-content-between mt-2" 
        v-for="(friend, index) in list"
        :key="index"
      >
        <img class="ms-3" :src="friend.profile_picture" :alt="profile_name">
        <h5> {{friend.profile_name}} </h5>
        <h6 class="me-3">Segui</h6>
      </div>
    </div>

    <Footer />
  </div>
</template>

<script>
import Profile from './Profile.vue';
import Footer from './Footer.vue';

export default {
  name: 'Right',
  components:{
    Footer, 
    Profile,
  },
  props:{
    list: Array,
  },
  
}
</script>

<style lang="scss" scoped>
  .right-content{
    height: 70vh;
    width: 40vw;
    background-color: red;
    .friend{
      height: 50%;
      background-color: rgb(245, 63, 94);
      overflow-y: auto;
      h2{
        font-size: 0.8rem;
        color: lightgrey;
      }
      h5{
        font-size: 0.9rem;
        color: rgb(94, 91, 91);
        cursor: pointer;
        &:hover{
          color: black;
        }
      }
      h6{
        cursor: pointer;
        color: rgb(137, 137, 250);
        font-size: 0.7rem;
        &:hover{
          transform: scale(1.05);
          color: rgb(56, 56, 252);
        }
      }
      img{
        width: 35px;
        height: 35px;
        border-radius: 999px;
        border: 2px solid rgb(172, 39, 39);
        cursor: pointer;
        &:hover{
          transform: scale(1.05);
        }
      }
    }
  }
</style>