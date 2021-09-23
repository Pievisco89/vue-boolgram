<template>
  <div class="nav d-flex">
    
    <div class="circle">

    </div>

    <div class="circle">
      
    </div>
    
    <div class="circle">
      
    </div>
    
  </div>
</template>

<script>
export default { 
  name: 'Navbar',

}
</script>

<style lang="scss">
  .nav{
    height: 10vh;
    width: 60vw;
    background-color: brown;
    .circle{
      height: 55px;
      width: 55px;
      border: 2px solid rgb(94, 92, 92);
      background-color: rgb(235, 229, 229);
      border-radius: 100px;
      margin-right: 0.8rem;
    }
  }
</style>