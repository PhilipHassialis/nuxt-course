<template>
  <div class="posts-page">
    <PostList :posts="loadedPosts" />
  </div>
</template>


<script>
import PostList from "@/components/Posts/PostList.vue";

export default {
  components: {
    PostList,
  },
  asyncData(context, callback) {
    setTimeout(() => {
      callback(null, {
        loadedPosts: [
          {
            id: "1",
            title: "Post 1",
            previewText:
              "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec auctor, nisl eget ultricies lacinia, nunc nisl ultricies nunc, nec",
            thumbnail: "https://picsum.photos/200/300?cache=1",
          },
          {
            id: "2",
            title: "Post 2",
            previewText:
              "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec auctor, nisl eget ultricies lacinia, nunc nisl ultricies nunc, nec",
            thumbnail: "https://picsum.photos/200/300?cache=2",
          },
        ],
      });
    }, 1500);
  },
};
</script>

<style scoped>
.posts-page {
  display: flex;
  justify-content: center;
  align-items: center;
}

.post-list {
  display: flex;
  padding: 20px;
  box-sizing: border-box;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
}
</style>