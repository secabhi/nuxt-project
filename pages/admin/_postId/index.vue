<template>
  <div class="admin-post-page">
    <section class="update-form">
      <AdminPostForm :post="loadedPost" />
    </section>
  </div>
</template>

<script>
import AdminPostForm from "@/components/admin/adminPostForm";
export default {
  layout: "admin",
  components: {
    AdminPostForm
  },
  data() {
    return {
      loadedPost: {
        author: "Abhi",
        title: "amazing",
        content: "super amazing",
        thumbnailLink:
          "https://img.freepik.com/free-vector/abstract-blue-technology-particle-background_1017-17494.jpg?size=626&ext=jpg"
      }
    };
  }
};
</script>

<style scoped>
.admin-post-page {
  padding: 20px;
  width: 60%;
  margin: auto;
}
</style>