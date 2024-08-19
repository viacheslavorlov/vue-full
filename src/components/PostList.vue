<template>
  <div class="flex gap-2 flex-col justify-center items-center">
    <h2 class="text-xl font-bold">Посты</h2>
    <post-item
      v-for="post in posts"
      :key="post.id"
      :post="post"
      class="border-2 border-blue-500"
    />
  </div>
</template>

<script>
import PostItem from "./PostItem.vue";
export default {
  components: { PostItem },
  props: {
    posts: {
      type: Array,
      required: true,
    },
  },
};
</script>
