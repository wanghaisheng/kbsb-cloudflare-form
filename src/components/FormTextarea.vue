<template>
  <div class="">
    <label class="block mr-4 mt-4" :for="id">{{ label }}</label>
    <textarea
      class="w-80 h-36 inline-block bg-gray-300 my-2 p-2"
      :id="id"
      :name="id"
      :minlength="minLength"
      :maxlength="maxLength"
      :required="isRequired"
      :placeholder="placeholder"
      :pattern="pattern"
    />
  </div>
</template>

<script>
export default {
  props: {
    id: String,
    label: String,
    placeholder: String,
    isRequired: {
      type: Boolean,
      default: false,
    },
    minLength: {
      type: String,
      default: '2',
    },
    maxLength: {
      type: String,
      default: '',
    },
    pattern: String,
  },
};
</script>
