<template>
  <div class="nav d-flex ps-3">
    
    <div class="circle mt-2"
      v-for="(story, index) in arrStories"
      :key="index"
    >
      <img class="img-fluid"  :src="story.profile_picture" :alt="story.profile_name">
      <h4 class="mt-1 text-capitalize"> {{story.profile_name}} </h4>
    </div>
    
  </div>
</template>

<script>
import axios from 'axios';

export default { 
  name: 'Navbar',
  data(){
    return{    
      arrStories: [],
    }
  },

  created(){
    axios.get('https://flynn.boolean.careers/exercises/api/boolgram/profiles')
      .then(resp =>{
        this.arrStories = resp.data;
        console.log(this.arrStories);
      })
      .catch(err => {
        console.log(err);
      })
  }
}

</script>

<style lang="scss" scoped>
  .nav{
    min-height: 12vh;
    width: 60vw;
    background-color: lightgrey;
    border-radius: 0.5rem 0.5rem 0 0;
    img{
      width: 5rem;
    }
    .circle{
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      width: 60px;
      border-radius: 100px;
      margin-right: 1.3rem;
      img{
        height: 50px;
        width: 50px;
        border: 2px solid rgb(172, 39, 39);
        border-radius: 100px;
        cursor: pointer;
        &:hover{
          transform: scale(1.05);
        }
      }
      h4{
        font-size: 0.5rem;
        cursor: pointer;
        color: rgb(94, 91, 91);
        &:hover{
          font-size: 0.6rem;
          color: black;
        }
      }
    }
  }
</style>