<template>
  <div>
    <section class="intro">
      <h1>Get the latest tech news</h1>
    </section>
    <section class="feature">
      <PostList />
    </section>
  </div>
</template>

<script>
import PostList from "@/components/posts/PostList";

export default {
  components: {
    PostList
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
