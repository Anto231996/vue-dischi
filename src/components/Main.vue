<template>
  <main class="py-5">
    <div class="container">
      <div class="row justify-content-center">
        <MainContent v-for="(element, index) in albumList" :key="index" :albumObject="element"/>
      </div>
    </div>
  </main>
</template>

<script>
import MainContent from './MainContent.vue';
import axios from 'axios';

export default {
  name: 'MainIndex',
  components:{
    MainContent
  },
  data: function(){
    return{
      albumList: null
    }
  },
  created: function(){
    this.getApiAlbum()
  },
  methods:{
    getApiAlbum(){
      axios
      .get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((result)=>{
        this.albumList = result.data.response
        console.log(this.albumList);
      })
      .catch((error)=>{
        console.log(error)
      })
    }
  }
}
</script>


<style scoped lang="scss">
  main{
    height: calc(100% - 80px);
    background-color: #1e2d3b;
  }
</style>