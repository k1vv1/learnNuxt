<template>

  <div>
    <h2>News Index page</h2>
    <p>NewsId: {{$route.params.newsId}}</p>
    <ul>
      <li><a href="/">Home</a></li>
      <li><nuxt-link :to="{name: 'news-id', params: {id: 123, title: 'I am news'}}">news-1</nuxt-link></li>
      <li><a href="/news/czy">news-2</a></li>
    </ul>
  </div>
</template>

<script>
export default {
  transition: 'test'
}
</script>