<template>
  <div class="movietype">
    <ul>
      <li 
        v-for="list in movielist" 
        :key="list.id">
        <nuxt-link :to="`/movie/${$route.params.type}/${list.id}`">
          <img 
            :src="list.img" 
            alt="">
          <h3>{{ list.title }}</h3>
          <p>{{ list.genres.join(',') }}</p>
          <p>综合评分: {{ list.rating }}</p>
        </nuxt-link>
      </li>
    </ul>
  </div>
</template>
<script>
import axios from '~/plugins/axios.js'
export default {
  layout: 'headerlayout',
  asyncData(context,callback){
    axios.get(`${context.params.type}`).then(res=>{
      callback(null,{movielist:res.data})
    })
  }
}
</script>
<style scoped>
ul li{
  list-style: none;
  float: left;
}
.movietype{
  margin-top: 20px;
}
.movietype ul li{
  width: 270px;
  padding: 15px;
  margin-bottom: 10px;
}
.movietype ul li:hover{
  box-shadow: 0px 0px 0px 1px #ccc;
}
.movietype ul li a img{
  width: 100%;
  display: block;
}
</style>
