<template>
  <form @submit.prevent="onSave">
    <AppControlInput v-model="editedPost.author">Author name</AppControlInput>
    <AppControlInput v-model="editedPost.title">Title</AppControlInput>
    <AppControlInput v-model="editedPost.thumbnailLink">Thumbnail</AppControlInput>
    <AppControlInput control-type="textarea" v-model="editedPost.content">Author name</AppControlInput>
    <AppButton type="submit">Save</AppButton>
    <AppButton type="button" style="margin-left:10px;" btn-style="cancel" @click="onCancel">Cancel</AppButton>
  </form>
</template>

<script>
import AppButton from "@/components/UI/AppButton";
import AppControlInput from "@/components/UI/AppControlInput";
export default {
  name: "AdminPostForm",
  components: {
    AppButton,
    AppControlInput
  },
  props: {
    post: {
      type: Object,
      required: false
    }
  },
  data() {
    return {
      editedPost: this.post
        ? { ...this.post }
        : {
            author: "",
            title: "",
            thumbnailLink: "",
            content: ""
          }
    };
  },
  methods: {
    onSave() {
      console.log(this.editedPost);
    },
    onCancel() {
      this.$router.push("/admin");
    }
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