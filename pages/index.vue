<!-- <template>
  <Tutorial/>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script> -->


<template>
  <div class="container">
    <nuxt-link v-for="user in users['data']" :key="user.id" class="list-data" :to="'/user-detail/'+user.id"> 
      {{ user.id }} 
    </nuxt-link>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  async asyncData() {
    const { data } = await axios.get('https://reqres.in/api/users') 
    // console.log(data)
    return {users: data}
  }
}
</script>

<style scoped>
.container {
  width: 75%;
  margin: 50px auto;
  text-align: center;
}
.list-data {
  background: #ddd;
  display: inline-block;
  margin:10px;
  padding:10px;
}
</style>