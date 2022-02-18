<template>
  <button class="px-5 py-2 font-black border-2">{{ text }}</button>
</template>

<script>
export default {
  props: {
    text: String,
  },
};
</script>
