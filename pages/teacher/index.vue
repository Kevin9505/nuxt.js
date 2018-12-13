<template>
  <section class="container">
    <ul>
      <li 
        v-for="item in teacherList" 
        :key="item.id">
        我是老师页面
        <nuxt-link :to="`/teacher/${item.id}`">{{ item.name }}</nuxt-link>
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data(){
    return {
      teacherList:[
        {
          id:1,
          name:'jack'
        },
        {
          id:2,
          name:'rose'
        },
        {
          id:3,
          name:'tom'
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
