<template>
  <div class="moviedetail">
    <img 
      :src="moviedetail.img" 
      alt="">
    <h3>{{ moviedetail.title }}</h3>
    <p>豆瓣评分 : {{ moviedetail.rating>0?'moviedetail.rating':'暂无评分' }}</p>
    <p>上映时间 : {{ moviedetail.details[0].year }}</p>
    <p>{{ moviedetail.details[0].summary }}</p>
  </div>
</template>
<script>
import axios from '~/plugins/axios.js'
export default {
  asyncData(context,callback){
    axios.get(`${context.params.type}/${context.params.id}?_embed=details`)
      .then(res=>{
        callback(null,{moviedetail:res.data})
      })
  }
}
</script>
<style scoped>
.moviedetail{
  width: 300px;
  padding: 20px;
  box-sizing: border-box;
  text-align: center;
  margin: 30px auto;
  box-shadow: 0px 0px 0px 1px #ccc;
}
.moviedetail img{
  display: block;
  width: 100%;
}
.moviedetail h3{
  padding: 10px 0;
}
.moviedetail p{
  padding: 5px 0px;
}
</style>
