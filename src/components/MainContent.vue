<template>
  <div id="item-album" class="col">
    <img :src="albumObject.poster" class="p-3" :alt="albumObject.title">
    <div id="text-album" class="text-center">
      <h5 class="text-white">{{albumObject.title}}</h5>
      <p class="text-secondary">{{albumObject.author}}</p>
      <p class="text-secondary">{{albumObject.year}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MainIndexContent',
  props: ['albumObject']
}
</script>


<style scoped lang="scss">
  div#item-album{
    background-color: #2e3a46;
    margin: 20px;
    flex: 0 1 calc(20% - 40px);
    
    img{
      width: 200px;
      height: 200px;
    }
  }
</style>