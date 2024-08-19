<template>
  <form
    @submit.prevent
    class="flex gap-2 flex-col justify-center items-center pt-10"
  >
    <input
      type="text"
      class="border border-black rounded-sm px-2 py-1 w-full"
      required
      v-model="post.title"
    />
    <textarea
      name=""
      id=""
      required
      cols="30"
      rows="10"
      class="border border-black rounded-sm px-2 py-1 w-full"
      v-model="post.body"
    ></textarea>
    <button
      @click="createPost"
      class="border border-black rounded-sm px-2 py-1 w-full"
    >
      Добавить
    </button>
  </form>
</template>

<script>
export default {
  data() {
    return {
      post: {
        title: "",
        body: "",
      },
    };
  },
  methods: {
    createPost() {
      this.post.id = Date.now();
      this.$emit("create", this.post);
      this.post = {
        title: "",
        body: "",
      };
    },
  },
};
</script>

<style></style>
