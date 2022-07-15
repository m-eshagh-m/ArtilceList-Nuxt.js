<template>
    <section>
      <h1>Get article title</h1>
      <div>
        <ul>
          <li v-for="article in articles" :key="article.id" class="item" >
            <nuxt-link :to="'/' + article.id">{{ article.title }}</nuxt-link>
          </li>
        </ul>
      </div>
    </section>
</template>

<script>
export default {
    props:{
        articles: {
            type: Array,
            required: true
        }
    }
}
</script>