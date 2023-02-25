<!-- <template>
  <div>

    <div>
      <b-navbar toggleable="lg" type="light" variant="light" class="shadow-md" fixed="top">
        <b-navbar-brand to="/">NUXT CRUD</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item to="/post">POST</b-nav-item>
            <b-nav-item href="https://santrikoding.com/ebook">EBOOK</b-nav-item>
            <b-nav-item href="https://santrikoding.com/kelas">COURSE</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>

    <Nuxt />
  </div>
</template>

<style>
body{
  background-color: lightgray;
}
.mt-5 {
  margin-top: 100px!important;
}
</style>
 -->

<template>
  <div class="container">
    <ul class="menu">
      <li> <nuxt-link to="/"> Home </nuxt-link> </li>
      <li> <nuxt-link to="/test"> Test </nuxt-link> </li>
    </ul>
    <nuxt/>
  </div>
</template>

<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}
*, *:before, *:after {
  box-sizing: border-box;
  margin: 0;
}
.container {
  width: 75%;
  margin: 100px auto;
  text-align: center;
}
.menu {
   list-style: none;
   margin-bottom: 0px;
}
.menu li {
  display: inline;
}
.menu li a {
  padding: 20px;
  text-decoration: none;
}
</style>
