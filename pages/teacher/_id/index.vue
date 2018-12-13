<template>
  <section class="container">
    {{ this.$route.params.id }}老师
  </section>
</template>

<script>
export default {
  data(){
    return{}
  },
  validate(value){
    return /^\d+$/.test(value.params.id)
  }
}
</script>

<style scoped>
</style>
