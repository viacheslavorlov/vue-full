<template>
  <div>
    <div class="flex gap-2 flex-col justify-start items-center">
      <h2 class="text-xl font-bold">{{ post.title }}</h2>
      <p>{{ post.body }}</p>
    </div>
    <button class="border-2 border-blue-500">Удалить</button>
  </div>
</template>

<script>
export default {
  props: {
    post: {
      type: Object,
      required: true,
    },
  },
};
</script>
