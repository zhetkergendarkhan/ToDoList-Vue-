<template>
<div>
  <h2>Home Page</h2>
  <p>Welcome to the first App written in Vue.js by me(and by internet of course)</p>
  <router-link to="/todos" class="router-link">Todos</router-link>
</div>
</template>

<script>
export default {
name: "Home"
}
</script>

<style>
.router-link{
  font-size: 20px;
  text-decoration: none;
  color: #cf0000;
}
.router-link:hover{
  color: #2c3e50;
  transition: color .2s linear;
  text-decoration: underline;
}
</style>
