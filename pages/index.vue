<template>
  <main>
    <div class="container">
      <section
        v-for="post in posts"
        :key="post.fields.slug"
      >
        <post
          :post="post"
        />
      </section>
    </div>
  </main>
</template>

<script>
import Post from '~/components/Post'

export default {
  components: {
    Post
  },
  computed: {
    posts() {
      return this.$store.state.posts;
    }
  }
};
</script>

<style lang="scss" scoped>
section + section {
  border-top: 1px solid;
  margin: 60px -15px 0;
  padding: 25px 15px 0;
}
</style>
