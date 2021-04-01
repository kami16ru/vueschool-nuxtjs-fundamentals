<template>
  <div class="container">
    <article>
      <h1 class="title">
        {{ post.title }}
      </h1>
      <p>{{ post.content }}</p>
    </article>
  </div>
</template>

<script>
export default {
  name: 'ShowPost',
  data () {
    return {
      id: this.$route.params.id,
      posts: [
        {
          id: 'balut',
          title: 'What is Balut?',
          content: 'balgjasdlfa;sdgjasd;gj'
        },
        {
          id: 'balut2231',
          title: 'What is Balut11111?',
          content: 'balgjasdlfa;sdgjasd;gj111'
        },
        {
          id: 'balutfasd',
          title: 'What is Balutfdsafdas?',
          content: 'balgjasdlfa;sdgjasd;gj1123213'
        },
        {
          id: 'bal00ut32100000',
          title: 'What is Balut312312312?',
          content: 'balgjasdlfa;sdgjasd;gjdagasdgasd'
        },
      ]
    }
  },
  computed: {
    post () {
      return this.posts.find(post => post.id === this.id)
    }
  }
}
</script>

<style scoped>

</style>
