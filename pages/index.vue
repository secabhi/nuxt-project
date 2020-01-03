<template>
  <div>
    <section class="intro">
      <h1>Get the latest tech news</h1>
    </section>
    <section class="feature">
      <PostPreview
        id="1"
        content="content bhai"
        title="Hello"
        thumbnail="https://img.freepik.com/free-vector/abstract-blue-technology-particle-background_1017-17494.jpg?size=626&ext=jpg"
      />
      <PostPreview
        id="2"
        content="content bhai 2"
        title="Hello 2"
        thumbnail="https://img.freepik.com/free-vector/abstract-blue-technology-particle-background_1017-17494.jpg?size=626&ext=jpg"
      />
      <PostPreview
        id="3"
        content="content bhai 2"
        title="Hello 2"
        thumbnail="https://img.freepik.com/free-vector/abstract-blue-technology-particle-background_1017-17494.jpg?size=626&ext=jpg"
      />
    </section>
  </div>
</template>

<script>
import PostPreview from "@/components/posts/postPreview";

export default {
  components: {
    PostPreview
  }
};
</script>

<style>
.intro {
  text-align: center;
  padding: 20px;
  background-color: #cecece;
}
</style>
