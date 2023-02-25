<!-- 
<template>
    <div>
    <h3>This is the GFG Page.</h3> 
    <NuxtLink to="/">
        Go to HomePage
    </NuxtLink>
    </div>
</template> -->

<template>
<!-- <h1> {{ name.toUpperCase() }} </h1> -->
  <div>
      <!-- <p> firstname : {{ user.firstname }} </p> -->
      <!-- <p> lastname   : {{ user.lastname }} </p>
      <p> avatar : {{ user.avatar }} </p> -->
  </div>

  <div>
    <h3>This is the User Detail Page.</h3>
    <NuxtLink to="/"> Go to HomePage </NuxtLink>
  </div>
</template>

<script>
import axios from "axios";
export default {
  async asyncData({ params }) {
    console.log("params: " + params.id);
    // const { data } = await axios.get('https://reqres.in/api/users/params.id')
    const { data } = await axios.get(`https://reqres.in/api/users/${params.id}`);
    // console.log(data['data']);
    if (!data.value) {
    //   throw createError({ statusCode: 404, statusMessage: "Page Not Found" });
    }
    return { user: data['data'], name: params.firstname };
  },
// function createError (err: { cause, data, message, name, stack, statusCode, statusMessage, fatal })
};
</script>

<style scoped>
div {
  margin-top: 30px;
}
</style>
