<template>
  <div class="headerlayout">
    <movieheader />
    <nuxt/>
  </div>
</template>
<script>
import movieheader from '~/components/movieheader.vue'
export default {
  components:{
    movieheader
  },
  data(){
    return{}
  }
}
</script>
