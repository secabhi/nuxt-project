<template>
  <div class="single-post-page">
    <section class="post">
      <h1>{{loadedPost.title}}</h1>
      <div class="post-details">
        <div>{{loadedPost.updatedDate}}</div>
        <div>{{loadedPost.author}}</div>
      </div>
    </section>
    <section class="post-feedback">
      <p>
        {{loadedPost.content}}
        <a href="mailto:feedback@gmail.com">feedback@gmail.com</a>
      </p>
    </section>
  </div>
</template>

<script>
export default {
  asyncData(context, callback) {
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        callback(null, {
          loadedPost: {
            id: "1",
            title: `first post ${context.route.params.id}`,
            content: "this is content",
            updatedDate: new Date(),
            author: "Abhi",
            thumbnail:
              "https://img.freepik.com/free-vector/abstract-blue-technology-particle-background_1017-17494.jpg?size=626&ext=jpg"
          }
        });
      });
    });
  }
};
</script>