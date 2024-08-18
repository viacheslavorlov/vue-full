<template>
  <div class="flex gap-2 flex-col justify-center items-center">
    <div v-for="post in posts" :key="post.id" class="border px-2 py-1 w-fit">
      <h2 class="text-xl font-bold">{{ post.title }}</h2>
      <p>{{ post.body }}</p>
    </div>
  </div>
</template>

<script>
export default {
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
};
</script>

<style></style>
