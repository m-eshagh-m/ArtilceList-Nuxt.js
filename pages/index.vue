<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <ArticleList :articles="articles" />
</template>

<script>
import axios from 'axios'

export default {
  async asyncData() {
    const { data } = await axios.get(
      'https://jsonplaceholder.typicode.com/posts/'
    )
    return { articles: data }
  },
}
</script>
