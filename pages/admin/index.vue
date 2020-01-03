<template>
  <div class="admin-page">
    <section class="new-post">
      <AppButton @click="$router.push('/admin/new-post')">Create Post</AppButton>
    </section>
    <section class="existing-post">
      <h1>Existing Posts</h1>
      <PostList isAdmin />
    </section>
  </div>
</template>

<script>
import PostList from "@/components/posts/postList";
import AppButton from "@/components/UI/AppButton";

export default {
  layout: "admin",
  components: {
    PostList,
    AppButton
  }
};
</script>

<style scoped>
.admin-page {
  padding: 20px;
}
.new-post {
  text-align: center;
  border-bottom: 2px solid #cecece;
  padding-bottom: 10px;
}
.existing-post h1 {
  text-align: center;
  padding: 10px;
  justify-content: center;
}
</style>