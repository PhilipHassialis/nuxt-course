<template>
  <section class="post-list">
    <PostPreview
      id="1"
      title="Hello there"
      previewText="my preview text"
      thumbnail="https://images.livemint.com/img/2023/01/01/1600x900/tech_1672594997400_1672595005161_1672595005161.jpg"
    />
    <PostPreview
      id="2"
      title="Second post"
      previewText="my second port"
      thumbnail="https://www.brookings.edu/wp-content/uploads/2017/11/metro_20171121_tech-empowers-tech-polarizes-mark-muro.jpg"
    />
  </section>
</template>

<script>
import PostPreview from "@/components/Posts/PostPreview.vue";

export default {
  components: {
    PostPreview,
  },
};
</script>

<style scoped>
.post-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>