<template>

  <header>
    <div class="logo-header">
      <img src="../assets/img/spotify-logo.png" alt="spotify logo">
    </div>
  </header>

</template>

<script>

export default {
  name: 'HeaderIndex',
}

</script>


<style scoped lang="scss">

  header{
    height: 80px;
    background-color: #2e3a46;

    div.logo-header{
      padding: 20px;
      
      img{
        width: 40px;
      }
    }
  }
  
</style>