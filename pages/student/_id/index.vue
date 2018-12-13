<template>
  <section class="container">
    {{ $route.params.id }}学生
  </section>
</template>

<script>
export default {
  data(){
    return{}
  },
  validate(value){
    // return /^\d+$/.test(value.params.id)
    return true
  }
}
</script>

<style scoped>
</style>
