<script>
export default {
  props: {
    article: {
      type: Object,
      defaultValue: {
        contentSnippet: '',
        image: {
          large: '',
          small: ''
        },
        isoDate: '',
        link: '',
        title: ''
      }
    }
  },
  data () {
    return {
      numValue: 6,
      calculated: 0,
      areaCode: 'XXY'
    }
  },
  computed: {
    computedValue () {
      return this.numValue + 7
    }
  }
}
</script>

<template>
  <div class="col-md-4">
    <div
      class="row g-0 border rounded overflow-hidden flex-md-row mb-4 shadow-sm h-md-250 position-relative"
    >
      <div class="col-12 d-lg-block">
        <img :src="article.image.small" alt="#">
      </div>
      <div class="col-12 p-4 d-flex flex-column position-static">
        <h4 class="mb-2">
          {{ article.title }}
        </h4>
        <p class="card-text mb-auto">
          {{ article.contentSnippet }}
        </p>
        <a href="#" class="stretched-link">Continue reading</a>
      </div>
    </div>
  </div>
</template>

<style scoped>
.article-img img {
  width: 100%;
}
</style>
