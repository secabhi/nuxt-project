<template>
  <nuxt-link :to="'/posts/'+  id">
    <article class="preview">
      <div class="thumbnail">
        <img :src="thumbnail" alt srcset />
      </div>
      <div class="content">
        <h1>{{title}}</h1>
        <p>{{content}}</p>
      </div>
    </article>
  </nuxt-link>
</template>

<script>
export default {
  name: "PostPreview",
  props: {
    id: {
      type: String,
      required: true
    },
    title: {
      type: String,
      required: true
    },
    content: {
      type: String,
      required: true
    },
    thumbnail: {
      type: String,
      required: true
    }
  }
};
</script>

<style scoped>
.preview {
  margin-top: 10px;
  border: 1px solid #ccc;
  box-shadow: 0 2px 2px #ccc;
  background-color: white;
  width: 90%;
  display: flex;
  margin: auto;
  border-collapse: collapse;
}
a {
  text-decoration: none;
  color: black;
}
.thumbnail {
  background-position: center;
  background-size: cover;
}
.content {
  padding: 10px 20px;
}
</style>