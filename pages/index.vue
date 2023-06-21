<script>
export default {
  data () {
    return {
      articles: []
    }
  },
  async fetch () {
    await this.$axios.get('v1/cnn-news')
      .then((res) => {
        this.articles = res.data.data
        console.log('Artikel', this.articles)
      })
  }
}
</script>

<template>
  <div id="app">
    <PageHeader />
    <main class="container">
      <AppHero />
      <div class="row mb-2">
        <CardArticle v-for="article in articles" :key="article.link" :article="article"/>
      </div>
    </main>
  </div>
</template>

<style>

</style>
