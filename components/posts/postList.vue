<template>
  <div class="container">
    <PostPreview
      v-for="post in posts"
      :key="post.id"
      :id="post.id"
      :content="post.content"
      :is-admin="isAdmin"
      :title="post.title"
      :thumbnail="post.thumbnail"
    />
  </div>
</template>

<script>
import PostPreview from "@/components/posts/postPreview";

export default {
  name: "PostList",
  components: {
    PostPreview
  },
  props: {
    isAdmin: {
      type: Boolean,
      default: false
    },
    posts: {
      type: Array,
      required: true
    }
  }
};
</script>

<style scoped>
.container {
  padding: 0 20px;
  margin: auto;
}
</style>