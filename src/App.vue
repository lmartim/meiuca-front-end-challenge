<template>
  <div>

    <h1>Meiuca Front-end Challenge</h1>
    <div class="wrapper">
      <CardContent
        v-for="(article, key) in articles"
        :key="key"
        :title="article.title"
        :content="article.description"
        buttonLabel="Ir para notícia"
        :buttonLink="article.url"
      />
    </div>
  </div>
</template>

<script>
import axios from 'axios'

import CardContent from '@bit/lmartim.shepherd.card-content'

export default {
  name: 'App',
  components: {
    CardContent
  },
  data() {
    return {
      articles: []
    }
  },
  async mounted() {
    const { data: { articles } } = await axios.get('http://newsapi.org/v2/top-headlines?sources=google-news-br&apiKey=ca8a3764d0fd47e9b4344c0e3bb2bb0a')
    this.articles = articles
  }
}
</script>

<style lang="scss">
.wrapper {
  display: grid;
  grid-template-columns: 48% 48%;
  justify-content: center;
  column-gap: 10px;
  row-gap: 10px;
}
</style>
