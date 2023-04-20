<template>
  <div class="admin-post-page">
    <section class="update-form">
      <AdminPostForm :post="loadedPost" />
    </section>
  </div>
</template>

<script>
import AdminPostForm from "@/components/Admin/AdminPostForm.vue";

export default {
  name: "AdminNewPostPage",
  components: {
    AdminPostForm,
  },
  data() {
    return {
      loadedPost: {
        author: "Philip",
        title: "My First Post",
        content: "This is my first post!",
        thumbnailLink:
          "https://www.rolandberger.com/img/og/roland_berger_ins_928_ces_2023_og.jpg",
      },
    };
  },
};
</script>

<style scoped>
.update-form {
  width: 90%;
  margin: 20px auto;
}

@media (min-width: 768px) {
  .update-form {
    width: 500px;
  }
}
</style>