<template>
  <div class="container">
    <PostPreview
      id="1"
      content="content bhai"
      :is-admin="isAdmin"
      title="Hello"
      thumbnail="https://img.freepik.com/free-vector/abstract-blue-technology-particle-background_1017-17494.jpg?size=626&ext=jpg"
    />
    <PostPreview
      id="2"
      content="content bhai 2"
      :is-admin="isAdmin"
      title="Hello 2"
      thumbnail="https://img.freepik.com/free-vector/abstract-blue-technology-particle-background_1017-17494.jpg?size=626&ext=jpg"
    />
    <PostPreview
      id="3"
      content="content bhai 2"
      :is-admin="isAdmin"
      title="Hello 2"
      thumbnail="https://img.freepik.com/free-vector/abstract-blue-technology-particle-background_1017-17494.jpg?size=626&ext=jpg"
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