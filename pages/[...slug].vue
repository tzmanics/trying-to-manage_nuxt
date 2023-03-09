<template>
  <main>
    <NuxtLink to='/'>HOMiE</NuxtLink>
    <hr>
    <ContentDoc />
  </main>
</template>
<style scoped>
  a {
    color: black;
    text-decoration: none;
  }
  a:visited {
    color: black;
    text-decoration: none;
  }
  a:hover {
    color: gray;
    text-decoration: none;
  }
  main {
    font-size: 20px;
    margin: 0 auto;
    min-width: 450px;
    width: 60%;
  }
  ul, li {
    margin-left: 40px;
  }
</style>