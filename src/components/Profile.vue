<template>
  <div class="profile d-flex align-items-center">
    <img src="../assets/img/profile.jpg" alt="profile">
    <h3>Sceriffo Woody</h3>
  </div>
</template>

<script>
export default {
  name: 'Profile'
}
</script>

<style lang="scss" scoped>
  .profile{
    height: 20%;
    background-color: rgb(131, 131, 250);
    img{
      height: 55px;
      width: 55px;
      border-radius: 999px;
      margin: 0 1.5rem;
      cursor: pointer;
    }
    h3{
      font-size: 1.2rem;
      color: rgb(94, 91, 91);
      cursor: pointer;
      &:hover{
        color: black;
      }
    }
  }
</style>