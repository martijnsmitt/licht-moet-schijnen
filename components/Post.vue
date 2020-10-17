<template>
  <div
    v-if="post.fields"
    class="post"
  >
    <img
      v-if="post.fields.heroImage"
      class="post-hero"
      :src="post.fields.heroImage.fields.file.url"
    />
    <p
      v-if="post.fields.description"
      class="post-description"
    >
      {{ post.fields.description }}
    </p>
    <article
      v-if="post.fields.body"
      v-html="$md.render(post.fields.body)"
      class="post-article"
    ></article>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      default: () => {}
    }
  }
};
</script>

<style lang="scss" scoped>
.post {
  &-hero {
    border-radius: 15px;
    max-width: 100%;
    margin: 60px 0 42px;
  }
}
</style>
