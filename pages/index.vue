<script setup>
const { path } = useRoute()
const { data } = await useAsyncData(`content-${path}`, () => {
  return queryContent().find()
})
</script>
<template>
  <main>
    <header>
      <h1 class="logo">Trying to Manage</h1>
      <h3><a href="https://www.youtube.com/watch?v=vjW8wmF5VWc">
        Watch me work, watch me try to be a good manager.
      </a></h3>
      <nav>
        <ul>
          <li class="nav-button">
            <NuxtLink to="/vision-statement" > Vision Statement </NuxtLink>
          </li>
        </ul>
      </nav>
    </header>
    <div class="blog-post-list">
      <ul class="post-list">
        <li v-for="post in data" :key="post.title">
          <NuxtLink :to="post._path">
            <div class="post-card">
              <h2 class="post-title">{{ post.title }}</h2>
              <p class="post-description"> {{ post.description}}</p>
            </div>
          </NuxtLink>
        </li>
      </ul>
    </div>
  </main>
</template>
<style>
  a {
    color: black;
    text-decoration: none;
  }
  a:visited {
    color: black;
    text-decoration: none;
  }
  a:hover {
    color: black;
    text-decoration: none;
  }
  h1 {
    margin-bottom:0;
  }
  h3 {
    margin-top: 0;
    font-size: smaller;
  }
  .nav-button {
    background: gray;
    border: 3px solid black;
    list-style: none;
    text-align: center;
    width: 120px;
  }
</style>