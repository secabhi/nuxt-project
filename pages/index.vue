<template>
  <div>
    <section class="intro">
      <h1>Get the latest tech news</h1>
    </section>
    <section class="feature">
      <PostList :posts="loadedPosts" />
    </section>
  </div>
</template>

<script>
import PostList from "@/components/posts/PostList";

export default {
  components: {
    PostList
  },
  data() {
    return {
      loadedPosts: [
        {
          id: "1",
          title: "first post",
          content: "this is content",
          thumbnail:
            "https://img.freepik.com/free-vector/abstract-blue-technology-particle-background_1017-17494.jpg?size=626&ext=jpg"
        },
        {
          id: "2",
          title: "first post 2",
          content: "this is content 2",
          thumbnail:
            "https://img.freepik.com/free-vector/abstract-blue-technology-particle-background_1017-17494.jpg?size=626&ext=jpg"
        },
        {
          id: "3",
          title: "first post 3",
          content: "this is content 3",
          thumbnail:
            "https://img.freepik.com/free-vector/abstract-blue-technology-particle-background_1017-17494.jpg?size=626&ext=jpg"
        }
      ]
    };
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
