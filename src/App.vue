<template>
  <div
    class="flex gap-2 flex-col justify-center items-center px-10 max-w-5xl mx-auto"
  >
    <div class="flex gap-2 flex-col justify-center items-center">
      <button class="border px-2 py-1 w-fit" @click="likes++">like</button>
      <button class="border px-2 py-1 w-fit" v-on:click="dislikes++">
        dislike
      </button>
    </div>
    <div>
      Количество лайков: <strong class="text-green-500">{{ likes }}</strong>
    </div>
    <div>
      Количество дизлайков: <strong class="text-red-500">{{ dislikes }}</strong>
    </div>
    <button>click me</button>
    <div class="flex gap-2 flex-col justify-center items-center">
      <input type="text" class="border border-black w-full" />
      <textarea
        class="border border-black w-full"
        name=""
        id=""
        cols="30"
        rows="10"
      ></textarea>
    </div>
  </div>
  <Posts />
</template>

<script>
export default {
  data() {
    return {
      likes: 0,
      dislikes: 0,
    };
  },
  methods: {
    addLike() {
      this.likes++;
    },
    addDislike() {
      this.dislikes++;
    },
  },
};
</script>
