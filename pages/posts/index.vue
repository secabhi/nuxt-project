<template>
  <div class="post-page">
    <PostList :posts="loadedPosts" />
  </div>
</template>

<script>
import PostList from "@/components/posts/PostList";
export default {
  components: {
    PostList
  },
  asyncData(context) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
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
        });
      }, 1000);
    })
      .then(data => {
        return data;
      })
      .catch(e => {
        context.error(e);
      });
  },
  created() {
    debugger;
    this.$store.dispatch("setPosts", this.loadedPosts);
  }
};
</script>

<style scoped>
.post-page {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>