<template>
  <section class="container">
    <ul>
      <li 
        v-for="item in studentList" 
        :key="item.id">
        我是学生页面
        <nuxt-link :to="`/student/${item.name}`">{{ item.name }}</nuxt-link>
      </li>
    </ul>
    <nuxt-child/>
  </section>
</template>

<script>
export default {
  data(){
    return {
      studentList:[
        {
          id:1,
          name:'大叔'
        },
        {
          id:2,
          name:'十三'
        },
        {
          id:3,
          name:'大叔十三'
        }
      ]
    }
  }
}
</script>
<style scoped>
.container {
  min-height: 100vh;
}
</style>
