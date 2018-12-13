<template>
  <div class="movieheader">
    <nuxt-link to="/movie/in_theaters">即将上映</nuxt-link>
    <nuxt-link to="/movie/coming_soon">正在热映</nuxt-link>
    <nuxt-link to="/movie/top250">top250</nuxt-link>
  </div>
</template>
<script>
export default {
  data(){
    return{}
  }
}
</script>
<style scoped>
.movieheader{
  height: 60px;
  display: flex;
  align-items: center;
  text-align: center;
  background-color: #14131b;
}
.movieheader a{
  flex: 1;
  color: #fff;
  text-decoration: none;
}
.movieheader a:hover{
  color: rgb(131, 1, 1);
}
</style>
