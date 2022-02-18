<template>
  <button class="px-10 py-2 my-4 bg-slate-500 text-white font-medium border-2">
    {{ text }}
  </button>
</template>

<script>
export default {
  props: {
    text: String,
  },
};
</script>
