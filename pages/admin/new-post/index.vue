<template>
  <div class="admin-new-page-post">
    <section class="new-form">
      <AdminPostForm />
    </section>
  </div>
</template>

<script>
import AdminPostForm from "@/components/admin/adminPostForm";
export default {
  layout: "admin",
  components: {
    AdminPostForm
  }
};
</script>

<style scoped>
.admin-new-page-post {
  padding: 20px;
  width: 60%;
  margin: auto;
}
</style>