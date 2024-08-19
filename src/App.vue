<template>
  <div
    class="flex gap-2 flex-col justify-center items-center px-10 max-w-5xl mx-auto"
  >
    <post-form @create="createPost" />
    <post-list :posts="posts" />
  </div>
</template>

<script>
import PostList from "./components/PostList.vue";
import PostForm from "./components/PostForm.vue";
export default {
  components: { PostList, PostForm },
  data() {
    return {
      posts: [
        {
          id: 1,
          title: "Post 1",
          body: "Body 1",
        },
        {
          id: 2,
          title: "Post 2",
          body: "Body 2",
        },
        {
          id: 3,
          title: "Post 3",
          body: "Body 3",
        },
      ],
    };
  },
  methods: {
    createPost(post) {
      console.log(post);
      this.posts.push(post);
      // if (post.title !== "" && post.body !== "") {
      //   this.posts.push({
      //     id: Date.now(),
      //     title: this.title,
      //     body: this.body,
      //   });
      // }
    },
  },
};
</script>
