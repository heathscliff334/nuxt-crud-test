<template>
  <div>
      <h1> {{ name.toUpperCase() }} </h1>
      <p> firstname : {{ user.firstname }} </p>
      <p> lastname   : {{ user.lastname }} </p>
      <p> avatar : {{ user.avatar }} </p>
  </div>
</template>

<script>
import axios from 'axios'
export default {
    async asyncData ({params}) {
        const { data } = await axios.get('https://reqres.in/api/users/${params.user}')
        console.log(data)
        return { user: data[0], name: params.user }
    }
}
</script>

<style scoped>
div {
    margin-top:30px;
}
</style>