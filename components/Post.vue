<template>
  <div
    v-if="post.fields"
    class="post"
  >
    <h1 class="post-title">{{ post.fields.title }}</h1>
    <p
      v-if="post.fields.description"
      class="post-description"
    >
      {{ post.fields.description }}
    </p>
    <img
      v-if="post.fields.heroImage"
      class="post-hero"
      :src="post.fields.heroImage.fields.file.url"
    />
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
    margin-top: 15px;
  }
}
</style>
